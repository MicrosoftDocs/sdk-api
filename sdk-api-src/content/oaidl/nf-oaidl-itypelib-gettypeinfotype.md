---
UID: NF:oaidl.ITypeLib.GetTypeInfoType
title: ITypeLib::GetTypeInfoType (oaidl.h)
author: windows-sdk-content
description: Retrieves the type of a type description.
old-location: automat\itypelib_gettypeinfotype.htm
tech.root: automat
ms.assetid: 2e0924ee-41f1-4f0a-a491-40b92bd0711e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTypeInfoType, GetTypeInfoType method [Automation], GetTypeInfoType method [Automation],ITypeLib interface, ITypeLib interface [Automation],GetTypeInfoType method, ITypeLib.GetTypeInfoType, ITypeLib::GetTypeInfoType, _oa96_ITypeLib_GetTypeInfoType, automat.itypelib_gettypeinfotype, oaidl/ITypeLib::GetTypeInfoType
ms.topic: method
f1_keywords: 
 - "oaidl/ITypeLib.GetTypeInfoType"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ITypeLib.GetTypeInfoType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITypeLib::GetTypeInfoType


## -description


Retrieves the type of a type description.


## -parameters




### -param index [in]

The index of the type description within the type library.




### -param pTKind [out]

The <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ne-oaidl-typekind">TYPEKIND</a> enumeration value for the type description.


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
<dt><b>S_OK
</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The <i>index</i> parameter is outside the range of  to <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nf-oaidl-itypelib-gettypeinfocount">GetTypeInfoCount</a> - 1.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypelib">ITypeLib</a>
 

 

