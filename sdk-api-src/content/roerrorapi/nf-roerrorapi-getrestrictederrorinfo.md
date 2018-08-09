---
UID: NF:roerrorapi.GetRestrictedErrorInfo
title: GetRestrictedErrorInfo function
author: windows-sdk-content
description: Gets the restricted error information object set by a previous call to SetRestrictedErrorInfo in the current logical thread.
old-location: winrt\getrestrictederrorinfo.htm
old-project: WinRT
ms.assetid: CA459E57-90D5-44F6-A896-4E1C2FA0DC57
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetRestrictedErrorInfo, GetRestrictedErrorInfo function [Windows Runtime], roerrorapi/GetRestrictedErrorInfo, winrt.getrestrictederrorinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: roerrorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - combase.dll
 - API-MS-Win-Core-Winrt-error-l1-1-0.dll
 - API-MS-Win-Core-Winrt-error-l1-1-1.dll
api_name:
 - GetRestrictedErrorInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Combase.dll
req.irql: 
req.product: ADAM
---

# GetRestrictedErrorInfo function


## -description


Gets the restricted error information object set by a previous call to <a href="https://msdn.microsoft.com/3F4A62EF-ECD3-45FA-836D-77C510C43C5E">SetRestrictedErrorInfo</a> in the current logical thread.


## -parameters




### -param ppRestrictedErrorInfo [out]

The restricted error info object associated with the current thread.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The  restricted error object was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no restricted error object associated with the current thread. Any other error object is removed from the thread.

</td>
</tr>
</table>
 




## -remarks



Call the <b>GetRestrictedErrorInfo</b>  function to get the most recently set <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> object on the current thread in a Windows Store app.

Call the <a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a> function to save error information for the current thread. Call the <a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a> function to raise an exception, terminate the current process, and report the error to the Windows Error Reporting service (WER).

<b>GetRestrictedErrorInfo</b> transfers ownership of the error object to the caller and clears the error state for the thread. If the most recently set error object doesn't support the <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> interface, the error state for the thread is cleared, but no interface is returned to the caller.

The <b>GetRestrictedErrorInfo</b> retrieves the error object from the current thread and calls <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to find the <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> interface.  If <b>IRestrictedErrorInfo</b> isn't found, <b>GetRestrictedErrorInfo</b> returns <b>S_FALSE</b>.  In this case, the error object is removed from the thread. For more info, see <a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>.

Calling the <b>GetRestrictedErrorInfo</b>  function fails if <a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a> isn't the system implementation. To create an <b>IRestrictedErrorInfo</b> object, call  the <a href="https://msdn.microsoft.com/ED647880-5A18-4F75-B7E5-3B9BF36229D3">OriginateError</a>, <a href="https://msdn.microsoft.com/B0921292-1EEA-4154-8AB4-B654A9B31DA6">TransformError</a>, or <a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/03317526-8c4f-4173-bc10-110c8112676a">GetErrorInfo</a>



<a href="https://msdn.microsoft.com/1af8d4bf-1217-44ca-b0dd-9a6feda16100">IRestrictedErrorInfo</a>



<a href="https://msdn.microsoft.com/345E1C4D-4A2F-4E18-9E70-4B8AE25FE8FD">RO_ERROR_REPORTING_FLAGS</a>



<a href="https://msdn.microsoft.com/4102CAD6-B5EC-4633-91CC-D56F6C0E287E">RoCaptureErrorContext</a>



<a href="https://msdn.microsoft.com/1BD47795-1B5E-42A4-B88F-7DE5160668E7">RoFailFastWithErrorContext</a>



<a href="https://msdn.microsoft.com/3F4A62EF-ECD3-45FA-836D-77C510C43C5E">SetRestrictedErrorInfo</a>
 

 

