---
UID: NF:vswriter.IVssWMFiledesc.GetFilespec
title: IVssWMFiledesc::GetFilespec method
author: windows-driver-content
description: The GetFilespec method returns the file specification used to obtain the list of files that the current IVssWMFiledesc object is a member of.
old-location: base\ivsswmfiledesc_getfilespec.htm
old-project: VSS
ms.assetid: 9661d22b-5c82-412d-966d-83605c568e22
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetFilespec method [VSS], GetFilespec method [VSS], IVssWMFiledesc interface, GetFilespec,IVssWMFiledesc.GetFilespec, IVssWMFiledesc, IVssWMFiledesc interface [VSS], GetFilespec method, IVssWMFiledesc::GetFilespec, _win32_ivsswmfiledesc_getfilespec, base.ivsswmfiledesc_getfilespec, vswriter/IVssWMFiledesc::GetFilespec
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VssApi.lib
-	VssApi.dll
api_name:
-	IVssWMFiledesc.GetFilespec
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWMFiledesc::GetFilespec method


## -description


The 
<b>GetFilespec</b> method returns the file specification used to obtain the list of files that the current 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object is a member of.

A querying method used a path and this file specification to return the current 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object.


## -parameters




### -param pbstrFilespec [out]

The address of a caller-allocated variable that receives a string specifying the returned file specification. 




A file specification cannot contain directory specifications (for example, no backslashes) but can contain the ? and * wildcard characters.


## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Successfully returned the filespec information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameter values is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The caller is out of memory or other system resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_INVALID_XML_DOCUMENT</b></dt>
</dl>
</td>
<td width="60%">
The XML document is not valid. Check the event log for details. For more information, see 
<a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">

        Unexpected error. The error code is logged in the error log file. For more information, see 
        <a href="https://msdn.microsoft.com/6377d937-5739-45f5-9195-5d18be4069ce">Event and Error Handling Under VSS</a>.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This value is not supported until Windows Server 2008 R2 and Windows 7. E_UNEXPECTED is used instead.

</td>
</tr>
</table>
 




## -remarks



The caller must call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory held by the <i>pbstrFilespec</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a>
 

 

