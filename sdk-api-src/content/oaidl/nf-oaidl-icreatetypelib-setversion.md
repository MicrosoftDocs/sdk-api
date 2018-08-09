---
UID: NF:oaidl.ICreateTypeLib.SetVersion
title: ICreateTypeLib::SetVersion
author: windows-sdk-content
description: Sets the major and minor version numbers of the type library.
old-location: automat\icreatetypelib_setversion.htm
old-project: automat
ms.assetid: 1c71bf8f-998a-4a9a-a4a8-981f51334cbe
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ICreateTypeLib interface [Automation],SetVersion method, ICreateTypeLib.SetVersion, ICreateTypeLib::SetVersion, SetVersion, SetVersion method [Automation], SetVersion method [Automation],ICreateTypeLib interface, _oa96_ICreateTypeLib_SetVersion, automat.icreatetypelib_setversion, oaidl/ICreateTypeLib::SetVersion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oaidl.h
req.include-header: 
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
 - ICreateTypeLib.SetVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ICreateTypeLib::SetVersion


## -description


Sets the major and minor version numbers of the type library.


## -parameters




### -param wMajorVerNum [in]

The major version number for the library.


### -param wMinorVerNum [in]

The minor version number for the library.


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
<dt><b>TYPE_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
The state of the type library is not valid for this operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>
 

 

