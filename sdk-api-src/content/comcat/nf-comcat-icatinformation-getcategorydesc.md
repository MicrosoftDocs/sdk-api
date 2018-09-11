---
UID: NF:comcat.ICatInformation.GetCategoryDesc
title: ICatInformation::GetCategoryDesc
author: windows-sdk-content
description: Retrieves the localized description string for a specific category ID.
old-location: com\icatinformation_getcategorydesc.htm
tech.root: com
ms.assetid: 66f004c2-2616-441e-8bb7-f56eb062bb35
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetCategoryDesc, GetCategoryDesc method [COM], GetCategoryDesc method [COM],ICatInformation interface, ICatInformation interface [COM],GetCategoryDesc method, ICatInformation.GetCategoryDesc, ICatInformation::GetCategoryDesc, _com_icatinformation_getcategorydesc, com.icatinformation_getcategorydesc, comcat/ICatInformation::GetCategoryDesc
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
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
 - ComCat.h
api_name:
 - ICatInformation.GetCategoryDesc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatInformation::GetCategoryDesc


## -description


Retrieves the localized description string for a specific category ID.


## -parameters




### -param rcatid [in]

The category identifier.


### -param lcid [in]

The locale.


### -param pszDesc [out]

A pointer to the string pointer for the description. This string must be released by the caller using the <a href="https://msdn.microsoft.com/en-us/library/ms680722(v=VS.85).aspx">CoTaskMemFree</a> function.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and S_OK, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CAT_E_CATIDNOEXIST</b></dt>
</dl>
</td>
<td width="60%">
The category ID <i>rcatid</i> is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CAT_E_NODESCRIPTION</b></dt>
</dl>
</td>
<td width="60%">
There is no description string for <i>rcatid</i> with the specified locale.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd542655(v=VS.85).aspx">ICatInformation</a>
 

 

