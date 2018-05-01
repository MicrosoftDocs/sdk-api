---
UID: NF:vswriter.IVssWMFiledesc.GetPath
title: IVssWMFiledesc::GetPath method
author: windows-driver-content
description: The GetPath method obtains the fully qualified directory path or the UNC path of the remote file share to obtain the list of files described in the current IVssWMFiledesc object.
old-location: base\ivsswmfiledesc_getpath.htm
old-project: VSS
ms.assetid: e646bf76-8779-4095-a022-2d69d5c3bead
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: GetPath method [VSS], GetPath method [VSS], IVssWMFiledesc interface, GetPath,IVssWMFiledesc.GetPath, IVssWMFiledesc, IVssWMFiledesc interface [VSS], GetPath method, IVssWMFiledesc::GetPath, _win32_ivsswmfiledesc_getpath, base.ivsswmfiledesc_getpath, vswriter/IVssWMFiledesc::GetPath
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
-	IVssWMFiledesc.GetPath
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssWMFiledesc::GetPath method


## -description


The 
<b>GetPath</b> method obtains the fully qualified directory path or the UNC path of the remote file share to obtain the list of files described in the current 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object.

A querying method used this path and a file specification to return the current 
<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a> object.


## -parameters




### -param pbstrPath [out]

The address of a caller-allocated variable that receives a <b>NULL</b>-terminated wide character string specifying the fully qualified directory path or the UNC path of the remote file share directory. 




The path can be a long or short file name and can use the prefix "\\?\". For more information, see 
<a href="https://msdn.microsoft.com/121cd5b2-e6fd-4eb4-99b4-b652d27b53e8">Naming a File</a>.

Users of this method need to check to determine whether this path ends with a backslash ("\").


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
Successfully returned the path information.

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



<b>Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003:  </b>Remote file shares are not supported until Windows 8 and Windows Server 2012.

The caller must call <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory held by the <i>pbstrPath</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/0b86882d-af1b-4a09-8c25-5b806c9ca909">IVssWMFiledesc</a>
 

 

