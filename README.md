github.com/apache/arrow/issues/50919
https://tracker.ceph.com/issues/81667#change-376227 
إيه اللي نعرفه من وصف الـ Bug؟
- المشروع الفرعي: RGW — بوابة تخزين الكائنات في Ceph.
- الجزء المعني: Multisite metadata synchronization.
- العملية المتسببة في المشكلة: مزامنة تغييرات أسماء المستخدمين، وقد تشمل المجموعات والأدوار أيضًا.
- الخطأ الظاهر: EEXIST، أي إن الاسم المطلوب موجود بالفعل.
- الأثر: عمليات المزامنة تفضل تفشل، وبالتالي بعض سجلات الـ metadata log لا يمكنها إكمال دورة التنظيف (trim).


# kubeedge issue:

https://github.com/kubeedge/kubeedge/pull/7226  
