---
UID: NI:pwm.IOCTL_PWM_CONTROLLER_GET_INFO
title: IOCTL_PWM_CONTROLLER_GET_INFO (pwm.h)
description: Retrieves information about a Pulse Width Modulation (PWM) controller. This information does not change after the controller is initialized.
helpviewer_keywords: ["IOCTL_PWM_CONTROLLER_GET_INFO","IOCTL_PWM_CONTROLLER_GET_INFO control","IOCTL_PWM_CONTROLLER_GET_INFO control code","base.ioctl_pwm_controller_get_info","pwm/IOCTL_PWM_CONTROLLER_GET_INFO"]
old-location: base\ioctl_pwm_controller_get_info.htm
tech.root: base
ms.assetid: C198FCCA-E1C5-4B03-8F42-7EE1952DC055
ms.date: 12/05/2018
ms.keywords: IOCTL_PWM_CONTROLLER_GET_INFO, IOCTL_PWM_CONTROLLER_GET_INFO control, IOCTL_PWM_CONTROLLER_GET_INFO control code, base.ioctl_pwm_controller_get_info, pwm/IOCTL_PWM_CONTROLLER_GET_INFO
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCTL_PWM_CONTROLLER_GET_INFO
 - pwm/IOCTL_PWM_CONTROLLER_GET_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - IOCTL_PWM_CONTROLLER_GET_INFO
---

# IOCTL_PWM_CONTROLLER_GET_INFO IOCTL


## -description

Retrieves information about a Pulse Width Modulation (PWM) controller. This information does not change after the controller is initialized.

## -ioctlparameters

### -input-buffer

Not used with this operation; set to NULL.

### -input-buffer-length

Not used with this operation; set to zero.

### -output-buffer

A pointer to a buffer that contains a <a href="/windows/desktop/api/pwm/ns-pwm-pwm_controller_info">PWM_CONTROLLER_INFO</a> struct. This represents the static information that characterizes a Pulse Width Modulation (PWM) controller.

### -output-buffer-length

The size of the output buffer must be exactly equal to the size of the requested <a href="/windows/desktop/api/pwm/ns-pwm-pwm_controller_info">PWM_CONTROLLER_INFO</a> struct. Every newer PWM_CONTROLLER_INFO version has a byte size that is greater than that of the previous version.

### -in-out-buffer


### -inout-buffer-length


### -status-block

If the operation completes successfully, 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> returns a nonzero 
       value.

If the operation fails or is pending, 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> returns zero. To get extended error 
       information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

To perform this operation, call the <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
   function with the following parameters.


<pre class="syntax">BOOL 
   WINAPI 
   DeviceIoControl( (HANDLE)       hDevice,         // handle to device
                    (DWORD)        IOCTL_PWM_CONTROLLER_GET_INFO, // dwIoControlCode(LPDWORD)      NULL,      // input buffer
                    (DWORD)        0,   // size of input buffer
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
      <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function.

</td>
</tr>
<tr>
<td width="40%">
<a id="dwIoControlCode__in__"></a><a id="dwiocontrolcode__in__"></a><a id="DWIOCONTROLCODE__IN__"></a><i>dwIoControlCode</i> [in] 

</td>
<td width="60%">
The control code for the operation. Use 
      <a href="/windows/desktop/api/pwm/ni-pwm-ioctl_pwm_controller_get_actual_period">IOCTL_PWM_CONTROLLER_GET_ACTUAL_PERIOD</a> 
      for this operation.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpInBuffer"></a><a id="lpinbuffer"></a><a id="LPINBUFFER"></a><i>lpInBuffer</i>

</td>
<td width="60%">
Not used with this operation; set to NULL.

</td>
</tr>
<tr>
<td width="40%">
<a id="nInBufferSize__in__"></a><a id="ninbuffersize__in__"></a><a id="NINBUFFERSIZE__IN__"></a><i>nInBufferSize</i> [in] 

</td>
<td width="60%">
Not used with this operation; set to zero.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpOutBuffer___out_"></a><a id="lpoutbuffer___out_"></a><a id="LPOUTBUFFER___OUT_"></a><i>lpOutBuffer</i>  [out]

</td>
<td width="60%">
A pointer to a buffer that contains a <a href="/windows/desktop/api/pwm/ns-pwm-pwm_controller_info">PWM_CONTROLLER_INFO</a> struct. This represents the static information that characterizes a Pulse Width Modulation (PWM) controller.  

</td>
</tr>
<tr>
<td width="40%">
<a id="nOutBufferSize__in__"></a><a id="noutbuffersize__in__"></a><a id="NOUTBUFFERSIZE__IN__"></a><i>nOutBufferSize</i> [in] 

</td>
<td width="60%">
The size of the output buffer must be exactly equal to the size of the requested <a href="/windows/desktop/api/pwm/ns-pwm-pwm_controller_info">PWM_CONTROLLER_INFO</a> struct. Every newer PWM_CONTROLLER_INFO version has a byte size that is greater than that of the previous version.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpBytesReturned__out__"></a><a id="lpbytesreturned__out__"></a><a id="LPBYTESRETURNED__OUT__"></a><i>lpBytesReturned</i> [out] 

</td>
<td width="60%">
A pointer to a variable that receives the size of the data stored in the output buffer, in bytes.

If the output buffer is too small, the call fails, 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns 
       <b>ERROR_INSUFFICIENT_BUFFER</b>, and <i>lpBytesReturned</i> is zero.

If <i>lpOverlapped</i> is <b>NULL</b>, 
       <i>lpBytesReturned</i> cannot be <b>NULL</b>. Even when an operation 
       returns no output data and <i>lpOutBuffer</i> is <b>NULL</b>, 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
       makes use of <i>lpBytesReturned</i>. After such an operation, the value of 
       <i>lpBytesReturned</i> is meaningless.

If <i>lpOverlapped</i> is not <b>NULL</b>, 
       <i>lpBytesReturned</i> can be <b>NULL</b>. If this parameter is not 
       <b>NULL</b> and the operation returns data, <i>lpBytesReturned</i> is 
       meaningless until the overlapped operation has completed. To retrieve the number of bytes returned, call 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>. If the 
       <i>hDevice</i> parameter is associated with an I/O completion port, you can retrieve the 
       number of bytes returned by calling 
       <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus">GetQueuedCompletionStatus</a>.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpOverlapped__in_"></a><a id="lpoverlapped__in_"></a><a id="LPOVERLAPPED__IN_"></a><i>lpOverlapped</i> [in]

</td>
<td width="60%">
A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure.

If <i>hDevice</i> was opened without specifying 
       <b>FILE_FLAG_OVERLAPPED</b>, <i>lpOverlapped</i> is ignored.

If <i>hDevice</i> was opened with the <b>FILE_FLAG_OVERLAPPED</b> flag, 
       the operation is performed as an overlapped (asynchronous) operation. In this case, 
       <i>lpOverlapped</i> must point to a valid 
       <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that contains a handle to an 
       event object. Otherwise, the function fails in unpredictable ways.

For overlapped operations, <a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a> 
       returns immediately, and the event object is signaled when the operation has been completed. Otherwise, the 
       function does not return until the operation has been completed or an error occurs.

</td>
</tr>
</table>
 

If the buffer size is less than the size of the lowest structure version, the request is completed by using a IOCTL completion status of STATUS_BUFFER_TOO_SMALL. Otherwise, the driver assumes the highest structure version that can fit into the supplied output buffer and completes the request successfully.

## -see-also

<a href="/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol">DeviceIoControl</a>