BÀI 4: PHÂN TÍCH & LỰA CHỌN PROMPT HỌC KIẾN THỨC KỸ THUẬT NÂNG CAO
Đáp án lựa chọn

Chọn: Phương án B

Lý do lựa chọn phương án B

Phương án B là lựa chọn tối ưu nhất vì áp dụng đầy đủ các nguyên tắc học kiến thức kỹ thuật nâng cao:

1. Level-based Explanation (Giải thích theo nhiều cấp độ)

Prompt yêu cầu giải thích theo 2 cấp độ:

Người mới bắt đầu: sử dụng ví dụ thực tế, phép ẩn dụ dễ hiểu.
Senior Developer: sử dụng thuật ngữ chuyên môn như Aspect, Pointcut, JoinPoint, Advice.

Cách tiếp cận này giúp người học hiểu từ bản chất đến chuyên sâu.

2. Comparative Analysis (So sánh khái niệm)

Prompt yêu cầu so sánh:

AOP (Aspect-Oriented Programming)
OOP (Object-Oriented Programming)

Việc so sánh giúp hiểu rõ:

OOP giải quyết nghiệp vụ chính.
AOP xử lý các chức năng cắt ngang (Cross-cutting Concerns) như Logging, Security, Transaction. 3. Practical Examples (Ví dụ thực tiễn)

Prompt yêu cầu:

Ví dụ Spring Boot thực tế.
Sử dụng @Aspect, @Before, @After.
Có chú thích bằng tiếng Việt.

Điều này giúp người học không chỉ hiểu lý thuyết mà còn biết cách áp dụng vào dự án thực tế.

Đánh giá theo 5 thành phần Prompt
Thành phần Đánh giá
Vai trò System Architect giàu kinh nghiệm sư phạm
Mục tiêu Học và hiểu Spring AOP
Ngữ cảnh Dự án Spring Boot cần tự động ghi log
Ràng buộc Giải thích đa cấp độ, so sánh, ví dụ thực tế
Định dạng Chia thành 3 phần rõ ràng

=> Đây là prompt đầy đủ và hiệu quả nhất.

Lý do loại trừ các phương án khác
Phương án A

"Giải thích Spring AOP là gì và viết cho tôi một ví dụ ghi log bằng Spring AOP."

Nhược điểm:

Quá ngắn gọn.
Không yêu cầu giải thích theo nhiều cấp độ.
Không có phần so sánh AOP và OOP.
Dễ khiến AI trả lời sơ sài.

=> Phù hợp tra cứu nhanh nhưng chưa tối ưu cho việc học.

Phương án C

"Hãy viết một class Aspect trong Spring Boot để ghi log khi chạy ứng dụng. Giải thích cách cấu hình trong file pom.xml."

Nhược điểm:

Chỉ tập trung vào code.
Không giải thích bản chất AOP.
Không có phần so sánh khái niệm.
Người học có thể biết cách dùng nhưng không hiểu nguyên lý hoạt động.

=> Thiên về triển khai hơn là học kiến thức.

Mã nguồn Spring AOP ghi log
package com.example.aop;

import org.aspectj.lang.JoinPoint;
import org.aspectj.lang.annotation.Aspect;
import org.aspectj.lang.annotation.Before;
import org.aspectj.lang.annotation.After;
import org.springframework.stereotype.Component;

@Aspect
@Component
public class LoggingAspect {

    // Chạy trước tất cả phương thức trong package service
    @Before("execution(* com.example.service.*.*(..))")
    public void logBefore(JoinPoint joinPoint) {

        System.out.println(
                "[START] Method: "
                        + joinPoint.getSignature().getName());
    }

    // Chạy sau khi phương thức kết thúc
    @After("execution(* com.example.service.*.*(..))")
    public void logAfter(JoinPoint joinPoint) {

        System.out.println(
                "[END] Method: "
                        + joinPoint.getSignature().getName());
    }

}
Giải thích
@Aspect: Đánh dấu đây là lớp Aspect.
@Before: Thực thi trước khi phương thức được gọi.
@After: Thực thi sau khi phương thức hoàn thành.
JoinPoint: Chứa thông tin về phương thức đang được thực thi.
execution(...): Pointcut xác định phạm vi các phương thức cần áp dụng logging.
Ví dụ hoạt động

Khi gọi:

userService.createUser();

Console:

[START] Method: createUser
[END] Method: createUser

Nhờ Spring AOP, việc ghi log được thực hiện tự động cho toàn bộ Service mà không cần viết log thủ công trong từng class.

Kết luận

Phương án B là lựa chọn tốt nhất vì kết hợp đầy đủ:

Giải thích nhiều cấp độ (Level-based Explanation).
So sánh khái niệm (Comparative Analysis).
Ví dụ thực tiễn (Practical Examples).

Giúp người học vừa hiểu bản chất Spring AOP vừa biết cách áp dụng hiệu quả trong dự án Spring Boot thực tế.
