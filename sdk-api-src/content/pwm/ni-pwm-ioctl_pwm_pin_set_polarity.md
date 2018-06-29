---
UID: NI:pwm.IOCTL_PWM_PIN_SET_POLARITY
title: IOCTL_PWM_PIN_SET_POLARITY
author: windows-sdk-content
description: Sets the signal polarity of the pin or channel. The control code sets the signal polarity based on a PWM_PIN_SET_POLARITY_INPUT structure. The signal polarity is either Active High or Active Low, as defined in the PWM_POLARITY enumeration.
old-location: base\ioctl_pwm_pin_set_polarity.htm
old-project: DevIO
ms.assetid: 310014B5-9E2A-49E5-AB07-B23408D9570F
ms.author: windowssdkdev
ms.date: 04/03/2018
ms.keywords: IOCTL_PWM_PIN_SET_POLARITY, IOCTL_PWM_PIN_SET_POLARITY control, IOCTL_PWM_PIN_SET_POLARITY control code, base.ioctl_pwm_pin_set_polarity, pwm/IOCTL_PWM_PIN_SET_POLARITY
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PWM_POLARITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pwm.h
api_name:
 - IOCTL_PWM_PIN_SET_POLARITY
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IOCTL_PWM_PIN_SET_POLARITY IOCTL


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]


Sets the signal polarity of the pin or channel. The control code sets the signal polarity based on a <a href="https://msdn.microsoft.com/346F981E-DAE1-4CEE-86A6-4416E3C293DE">PWM_PIN_SET_POLARITY_INPUT</a> structure. The signal polarity is either Active High or Active Low, as  defined in the <a href="https://msdn.microsoft.com/D818E512-5E50-4CF2-AF22-1A4AB07679A6">PWM_POLARITY</a> enumeration.




## -ioctlparameters




### -input-buffer

A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/432C10EF-AC08-4781-9BCA-A31E0DF12704">PWM_PIN_GET_POLARITY_OUTPUT</a> structure. This represents the polarity value of the PWM controller, and is either Active High or Active Low.


### -input-buffer-length

The size of the input buffer, in bytes.


### -output-buffer

Not used with this operation; set to NULL.


### -output-buffer-length

Not used with this operation; set to zero.


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
                    (DWORD)        IOCTL_PWM_PIN_SET_POLARITY, // dwIoControlCode
                    (LPDWORD)      lpInBuffer,      // input buffer
                    (DWORD)        nInBufferSize,   // size of input buffer
                    (LPDWORD)      NULL,      // output buffer
                    (DWORD)        0,  // size of output buffer
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
      <b>IOCTL_PWM_PIN_SET_POLARITY</b> 
      for this operation.

</td>
</tr>
<tr>
<td width="40%">
<a id="lpInBuffer"></a><a id="lpinbuffer"></a><a id="LPINBUFFER"></a><i>lpInBuffer</i>

</td>
<td width="60%">
A pointer to a buffer that contains a <a href="https://msdn.microsoft.com/432C10EF-AC08-4781-9BCA-A31E0DF12704">PWM_PIN_GET_POLARITY_OUTPUT</a> structure. This represents the polarity value of the PWM controller, and is either Active High or Active Low.

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
Not used with this operation; set to NULL.

</td>
</tr>
<tr>
<td width="40%">
<a id="nOutBufferSize__in__"></a><a id="noutbuffersize__in__"></a><a id="NOUTBUFFERSIZE__IN__"></a><i>nOutBufferSize</i> [in] 

</td>
<td width="60%">
Not used with this operation; set to zero.

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
 

Changing polarity is only allowed when the pin is stopped. You can tell whether the pin is stopped by using the <a href="https://msdn.microsoft.com/library/Mt843917(v=VS.85).aspx">IOCTL_PWM_PIN_IS_STARTED</a> control code.

Changing polarity while a pin is started can lead to glitches on some Pulse Width Modulation (PWM) controllers. If you want to change polarity, stop the pin first, change the polarity, and then start the pin. 




## -see-also




<a href="https://msdn.microsoft.com/1d35c087-6672-4fc6-baa1-a886dd9d3878">DeviceIoControl</a>
 

 

