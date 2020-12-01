---
UID: NF:fltuser.FilterInstanceGetInformation
title: FilterInstanceGetInformation function (fltuser.h)
description: The FilterInstanceGetInformation function returns various kinds of information about a minifilter instance.
helpviewer_keywords: ["FilterInstanceGetInformation","FilterInstanceGetInformation function [Installable File System Drivers]","FltWin32ApiRef_e34f8425-037b-4c31-8559-2ad32527746f.xml","fltuser/FilterInstanceGetInformation","ifsk.filterinstancegetinformation"]
old-location: ifsk\filterinstancegetinformation.htm
tech.root: ifsk
ms.assetid: 222f5f68-6a1c-420e-a56f-de53b23f6ce6
ms.date: 12/05/2018
ms.keywords: FilterInstanceGetInformation, FilterInstanceGetInformation function [Installable File System Drivers], FltWin32ApiRef_e34f8425-037b-4c31-8559-2ad32527746f.xml, fltuser/FilterInstanceGetInformation, ifsk.filterinstancegetinformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterInstanceGetInformation
 - fltuser/FilterInstanceGetInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterInstanceGetInformation
---

# FilterInstanceGetInformation function


## -description

The <b>FilterInstanceGetInformation</b> function returns various kinds of information about a minifilter instance.

## -parameters

### -param hInstance [in]

Handle returned by a previous call to <a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>.

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
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceFullInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstancePartialInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a> structure for the instance. 

</td>
</tr>
<tr>
<td>
<b>InstanceAggregateStandardInformation</b>

</td>
<td>
Return an <a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a> structure for the instance.  The <b>LegacyFilter</b> portion of the structure is utilized starting with Windows 8.  This structure is available starting with Windows Vista.

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

<b>FilterInstanceGetInformation</b> is the Win32 equivalent of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltgetinstanceinformation">FltGetInstanceInformation</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterinstancecreate">FilterInstanceCreate</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltgetinstanceinformation">FltGetInstanceInformation</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_aggregate_standard_information">INSTANCE_AGGREGATE_STANDARD_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_basic_information">INSTANCE_BASIC_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_full_information">INSTANCE_FULL_INFORMATION</a>



<a href="/windows-hardware/drivers/ddi/content/fltuserstructures/ns-fltuserstructures-_instance_partial_information">INSTANCE_PARTIAL_INFORMATION</a>