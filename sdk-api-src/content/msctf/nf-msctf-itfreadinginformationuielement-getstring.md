---
UID: NF:msctf.ITfReadingInformationUIElement.GetString
title: ITfReadingInformationUIElement::GetString
author: windows-sdk-content
description: This method returns the string on the reading information UI.
old-location: tsf\itfreadinginformationuielement_getstring.htm
old-project: TSF
ms.assetid: d8e7dae5-ea73-4fad-a731-3ca1eaa60b03
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetString, GetString method [Text Services Framework], GetString method [Text Services Framework],ITfReadingInformationUIElement interface, ITfReadingInformationUIElement interface [Text Services Framework],GetString method, ITfReadingInformationUIElement.GetString, ITfReadingInformationUIElement::GetString, msctf/ITfReadingInformationUIElement::GetString, tsf.iitfreadinginformationuielement_getstring, tsf.itfreadinginformationuielement_getstring
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfReadingInformationUIElement.GetString
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfReadingInformationUIElement::GetString


## -description


This  method returns the string on the reading information UI.


## -parameters




### -param pstr [out]

[out] A pointer to the BSTR of the reading information string.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
</table>
 



