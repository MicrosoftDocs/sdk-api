---
UID: NI:pwm.IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD
title: IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD
author: windows-sdk-content
description: Sets the output signal period of a Pulse Width Modulation (PWM) controller to a suggested value.
old-location: base\ioctl_pwm_controller_set_desired_period.htm
tech.root: devio
ms.assetid: 7E25B3C8-8C73-4808-B460-DFC408A2482F
ms.author: windowssdkdev
ms.date: 10/02/2018
ms.keywords: IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD, IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD control, IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD control code, base.ioctl_pwm_controller_set_desired_period, pwm/IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: ioctl
req.header: pwm.h
req.include-header: Pwm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD IOCTL


## -description



Sets the output signal period of a Pulse Width Modulation (PWM) controller to a suggested value. 




## -ioctlparameters




### -input-buffer

A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/BD003CAE-3DB9-4C7B-9CAD-735866C17004">PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT</a> struct. The associated value is the requested output signal period, in picoseconds, for the controller. This value must be greater than zero (0). It must be in the controller supported range of periods, which is between the <b>MinimumPeriod</b> and <b>MaximumPeriod</b> values, inclusive, which you can obtain by using <a href="base.ioctl_ioctl_pwm_controller_get_info">IOCTL_PWM_CONTROLLER_GET_INFO</a>.


### -input-buffer-length

The size of the input buffer, in bytes.


### -output-buffer

 A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/BD003CAE-3DB9-4C7B-9CAD-735866C17004">PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT</a> struct. The associated value is the effective output signal period of the Pulse Width Modulation (PWM) controller. It can later be retrieved by using <a href="base.ioctl_ioctl_pwm_controller_get_actual_period">IOCTL_PWM_CONTROLLER_GET_ACTUAL_PERIOD</a>.  


### -output-buffer-length

The size of the output buffer, in bytes.


### -in-out-buffer



<text></text>




### -inout-buffer-length



<text></text>




### -status-block

If the operation completes successfully, 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> returns a nonzero 
       value.

If the operation fails or is pending, 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> returns zero. To get extended error 
       information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.


## -remarks



To perform this operation, call the <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
   function with the following parameters.


<pre class="syntax">BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD, // dwIoControlCode(LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      lpOutBuffer,     // output buffer
                    (DWORD)        nOutBufferSize,  // size of output buffer
                    (LPDWORD)      lpBytesReturned, // number of bytes returned
                    (LPOVERLAPPED) lpOverlapped );  // OVERLAPPED structure</pre>




<table>
<tr>
<th>Parameters</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="hDevice__in__"></a><a id="hdevice__in__"></a><a id="HDEVICE__IN__"></a><i>hDevice</i> [in] 

</td>
<td width="60%">
A handle to the device. To obtain a device handle, call the 
      <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function.

</td>
</tr>
<tr>
<td width="40%">
<a id="dwIoControlCode__in__"></a><a id="dwiocontrolcode__in__"></a><a id="DWIOCONTROLCODE__IN__"></a><i>dwIoControlCode</i> [in] 

</td>
<td width="60%">
The control code for the operation. Use 
      <b>IOCTL_PWM_CONTROLLER_SET_DESIRED_PERIOD</b> 
      for this operation.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpInBuffer"></a><a id="lpinbuffer"></a><a id="LPINBUFFER"></a><i>lpInBuffer</i>

</td>
<td width="60%">
A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/BD003CAE-3DB9-4C7B-9CAD-735866C17004">PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT</a> struct. The associated value is the requested output signal period, in picoseconds, for the controller. This value must be greater than zero (0). It must be in the controller supported range of periods, which is between the <b>MinimumPeriod</b> and <b>MaximumPeriod</b> values, inclusive, which you can obtain by using <a href="base.ioctl_ioctl_pwm_controller_get_info">IOCTL_PWM_CONTROLLER_GET_INFO</a>.

</td>
</tr>
<tr>
<td width="40%">
<a id="nInBufferSize__in__"></a><a id="ninbuffersize__in__"></a><a id="NINBUFFERSIZE__IN__"></a><i>nInBufferSize</i> [in] 

</td>
<td width="60%">
The size of the input buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpOutBuffer___out_"></a><a id="lpoutbuffer___out_"></a><a id="LPOUTBUFFER___OUT_"></a><i>lpOutBuffer</i>  [out]

</td>
<td width="60%">
 A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/BD003CAE-3DB9-4C7B-9CAD-735866C17004">PWM_CONTROLLER_SET_DESIRED_PERIOD_INPUT</a> struct. The associated value is the effective output signal period of the Pulse Width Modulation (PWM) controller. It can later be retrieved by using <a href="base.ioctl_ioctl_pwm_controller_get_actual_period">IOCTL_PWM_CONTROLLER_GET_ACTUAL_PERIOD</a>.

</td>
</tr>
<tr>
<td width="40%">
<a id="nOutBufferSize__in__"></a><a id="noutbuffersize__in__"></a><a id="NOUTBUFFERSIZE__IN__"></a><i>nOutBufferSize</i> [in] 

</td>
<td width="60%">
The size of the output buffer, in bytes.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpBytesReturned__out__"></a><a id="lpbytesreturned__out__"></a><a id="LPBYTESRETURNED__OUT__"></a><i>lpBytesReturned</i> [out] 

</td>
<td width="60%">
<b>LPDWORD</b>

A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

If the output buffer is too small, the call fails, 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns 
       <b>ERROR_INSUFFICIENT_BUFFER</b>, and <i>lpBytesReturned</i> is zero.

If <i>lpOverlapped</i> is <b>NULL</b>, 
       <i>lpBytesReturned</i> cannot be <b>NULL</b>. Even when an operation 
       returns no output data and <i>lpOutBuffer</i> is <b>NULL</b>, 
       <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
       makes use of <i>lpBytesReturned</i>. After such an operation, the value of 
       <i>lpBytesReturned</i> is meaningless.

If <i>lpOverlapped</i> is not <b>NULL</b>, 
       <i>lpBytesReturned</i> can be <b>NULL</b>. If this parameter is not 
       <b>NULL</b> and the operation returns data, <i>lpBytesReturned</i> is 
       meaningless until the overlapped operation has completed. To retrieve the number of bytes returned, call 
       <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>. If the 
       <i>hDevice</i> parameter is associated with an I/O completion port, you can retrieve the 
       number of bytes returned by calling 
       <a href="https://msdn.microsoft.com/8121a38b-0fe1-43b8-aed6-4b85af1feba9">GetQueuedCompletionStatus</a>.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpOverlapped__in_"></a><a id="lpoverlapped__in_"></a><a id="LPOVERLAPPED__IN_"></a><i>lpOverlapped</i> [in]

</td>
<td width="60%">
<b>LPOVERLAPPED</b>

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure.

If <i>hDevice</i> was opened without specifying 
       <b>FILE_FLAG_OVERLAPPED</b>, <i>lpOverlapped</i> is ignored.

If <i>hDevice</i> was opened with the <b>FILE_FLAG_OVERLAPPED</b> flag, 
       the operation is performed as an overlapped (asynchronous) operation. In this case, 
       <i>lpOverlapped</i> must point to a valid 
       <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that contains a handle to an 
       event object. Otherwise, the function fails in unpredictable ways.

For overlapped operations, <a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a> 
       returns immediately, and the event object is signaled when the operation has been completed. Otherwise, the 
       function does not return until the operation has been completed or an error occurs.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

