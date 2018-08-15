---
UID: NF:oaidl.ICreateTypeLib.SetHelpFileName
title: ICreateTypeLib::SetHelpFileName
author: windows-sdk-content
description: Sets the name of the Help file.
old-location: automat\icreatetypelib_sethelpfilename.htm
old-project: automat
ms.assetid: a9dc11b0-1483-4272-84cb-4f885f6cff6f
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICreateTypeLib interface [Automation],SetHelpFileName method, ICreateTypeLib.SetHelpFileName, ICreateTypeLib::SetHelpFileName, SetHelpFileName, SetHelpFileName method [Automation], SetHelpFileName method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetHelpFileName, automat.icreatetypelib_sethelpfilename, oaidl/ICreateTypeLib::SetHelpFileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oaidl.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VARKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeLib.SetHelpFileName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeLib::SetHelpFileName


## -description


Sets the name of the Help file.


## -parameters




### -param szHelpFileName [in]

The name of the Help file for the library.



## -returns



This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_INSUFFICIENTMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
</table>
 




## -remarks



Each type library can reference a single Help file.



The <a href="https://msdn.microsoft.com/aa65e143-47db-4241-9c66-fe3a1dcf1f0a">GetDocumentation</a> method of the created <a href="https://msdn.microsoft.com/c1e5d71f-6a4e-45f3-811d-f57024f81a55">ITypeLib</a> returns a fully qualified path for the Help file, which is formed by appending the name passed into <i>szHelpFileName</i> to the registered Help directory for the type library. The Help directory is registered under:



\TYPELIB\&lt;guid of library&gt;\&lt;Major.Minor version &gt;\HELPDIR





## -see-also




<a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>
 

 

