---
UID: NF:fltuser.FilterInstanceGetInformation
title: FilterInstanceGetInformation function
author: windows-sdk-content
description: The FilterInstanceGetInformation function returns various kinds of information about a minifilter instance.
old-location: ifsk\filterinstancegetinformation.htm
tech.root: ifsk
ms.assetid: 222f5f68-6a1c-420e-a56f-de53b23f6ce6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FilterInstanceGetInformation, FilterInstanceGetInformation function [Installable File System Drivers], FltWin32ApiRef_e34f8425-037b-4c31-8559-2ad32527746f.xml, fltuser/FilterInstanceGetInformation, ifsk.filterinstancegetinformation
ms.topic: function
req.header: fltuser.h
req.include-header: FltUser.h
req.target-type: Universal
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterInstanceGetInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FilterInstanceGetInformation function


## -description


The <b>FilterInstanceGetInformation</b> function returns various kinds of information about a minifilter instance. 


## -parameters




### -param hInstance [in]

Handle returned by a previous call to <a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>. 


### -param dwInformationClass [in]

The type of instance information structure returned.  This parameter must contain one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>
<b>InstanceBasicInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/35e2b098-1bc2-4ffc-86c8-b60b651df027">INSTANCE_BASIC_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceFullInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/6c034749-c110-4623-8a7b-a19235cad298">INSTANCE_FULL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstancePartialInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/cabcb39c-1f8d-41dc-a6ec-78f3fb3911cf">INSTANCE_PARTIAL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceAggregateStandardInformation</b>

</td>
<td>
Return an <a href="https://msdn.microsoft.com/35311ee7-d023-4b04-b510-a949ab9a40ca">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a> structure for the instance.  The <b>LegacyFilter</b> portion of the structure is utilized starting with Windows 8.  This structure is available starting with Windows Vista.

</td>
</tr>
</table>
 


### -param lpBuffer [out]

Pointer to a caller-allocated buffer that receives the requested information. The type of the information returned in the buffer is defined by the <i>dwInformationClass</i> parameter. 


### -param dwBufferSize [in]

Size, in bytes, of the buffer that the <i>lpBuffer</i> parameter points to. The caller should set this parameter according to the given <i>dwInformationClass</i>. 


### -param lpBytesReturned [out]

Pointer to a caller-allocated variable that receives the number of bytes returned in the buffer that <i>lpBuffer</i> points to if the call to <b>FilterInstanceGetInformation</b> succeeds. This parameter is required and cannot be <b>NULL</b>. 


## -returns



<b>FilterInstanceGetInformation</b> returns S_OK if successful. Otherwise, it returns an HRESULT error value, such as one of the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpBuffer</i> is not large enough to contain the requested information.  When this value is returned, <i>lpBytesReturned</i> will contain the size, in bytes, of the buffer required for the given <i>dwInformationClass</i> structure.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER)</b></dt>
</dl>
</td>
<td width="60%">
An invalid value was specified for the <i>dwInformationClass</i> parameter.  For example, if <b>InstanceAggregateStandardInformation</b> is specified for an operating system prior to Windows Vista, <b>FilterInstanceGetInformation</b> returns this HRESULT value.

</td>
</tr>
</table>
 




## -remarks



Given a handle to a minifilter instance, this routine returns information about the minifilter instance.  The type of instance information returned is determined by the <i>dwInformationClass</i> parameter.

<b>FilterInstanceGetInformation</b> is the Win32 equivalent of <a href="https://msdn.microsoft.com/eb8ba04a-dbf8-4964-8b45-2620447418b5">FltGetInstanceInformation</a>. 




## -see-also




<a href="https://msdn.microsoft.com/eb29fefc-285a-4a77-b1f6-1d42d029b7b7">FilterInstanceCreate</a>



<a href="https://msdn.microsoft.com/eb8ba04a-dbf8-4964-8b45-2620447418b5">FltGetInstanceInformation</a>



<a href="https://msdn.microsoft.com/35311ee7-d023-4b04-b510-a949ab9a40ca">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="https://msdn.microsoft.com/35e2b098-1bc2-4ffc-86c8-b60b651df027">INSTANCE_BASIC_INFORMATION</a>



<a href="https://msdn.microsoft.com/6c034749-c110-4623-8a7b-a19235cad298">INSTANCE_FULL_INFORMATION</a>



<a href="https://msdn.microsoft.com/cabcb39c-1f8d-41dc-a6ec-78f3fb3911cf">INSTANCE_PARTIAL_INFORMATION</a>
 

 

