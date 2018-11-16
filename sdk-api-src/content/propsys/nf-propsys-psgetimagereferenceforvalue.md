---
UID: NF:propsys.PSGetImageReferenceForValue
title: PSGetImageReferenceForValue function
author: windows-sdk-content
description: Gets an instance of a property description interface for a specified property.
old-location: properties\PSGetImageReferenceForValue.htm
tech.root: properties
ms.assetid: E37AF2ED-E3F9-4e50-9317-9DAF03AC543F
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSGetImageReferenceForValue, PSGetImageReferenceForValue function [Windows Properties], _shell_PSGetImageReferenceForValue, properties.PSGetImageReferenceForValue, propsys/PSGetImageReferenceForValue, shell.PSGetImageReferenceForValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propsys.h
req.include-header: Propsys.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetImageReferenceForValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- PSGetImageReferenceForValue
: 
---

# PSGetImageReferenceForValue function


## -description


Gets an instance of a property description interface for a specified property.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

A reference to a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure that specifies the property.


### -param propvar [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>.


### -param ppszImageRes [out]

Type: <b>void**</b>

When this function returns successfully, contains the interface pointer requested in <i>riid</i>.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>
 




## -remarks



We recommend that you use the <a href="https://msdn.microsoft.com/268B59FA-44EB-4777-8162-C50981CBDD09">IID_PPV_ARGS</a> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.



