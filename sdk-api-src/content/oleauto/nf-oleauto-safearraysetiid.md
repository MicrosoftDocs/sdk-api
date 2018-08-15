---
UID: NF:oleauto.SafeArraySetIID
title: SafeArraySetIID function
author: windows-sdk-content
description: Sets the GUID of the interface for the specified safe array.
old-location: automat\safearraysetiid.htm
old-project: automat
ms.assetid: 851b8a44-9da4-418c-88bc-80c9fc55d25c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: SafeArraySetIID, SafeArraySetIID function [Automation], _oa96_SafeArraySetIID, automat.safearraysetiid, oleauto/SafeArraySetIID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.redist: 
req.target-type: Windows
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArraySetIID
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# SafeArraySetIID function


## -description


Sets the GUID of the interface for the specified safe array. 


## -parameters




### -param psa [in]

The safe array descriptor.


### -param guid [in]

The IID.


## -returns



This function can return one of these values.

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
The argument <i>psa</i> is null or the array descriptor does not have the FADF_HAVEIID flag set.

</td>
</tr>
</table>
 



