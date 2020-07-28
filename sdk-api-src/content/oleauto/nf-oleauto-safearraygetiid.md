---
UID: NF:oleauto.SafeArrayGetIID
title: SafeArrayGetIID function (oleauto.h)
description: Gets the GUID of the interface contained within the specified safe array.
helpviewer_keywords: ["SafeArrayGetIID","SafeArrayGetIID function [Automation]","_oa96_SafeArrayGetIID","automat.safearraygetiid","oleauto/SafeArrayGetIID"]
old-location: automat\safearraygetiid.htm
tech.root: automat
ms.assetid: 9416f7f8-aee0-4e6a-be4f-ca6061adb244
ms.date: 12/05/2018
ms.keywords: SafeArrayGetIID, SafeArrayGetIID function [Automation], _oa96_SafeArrayGetIID, automat.safearraygetiid, oleauto/SafeArrayGetIID
f1_keywords:
- oleauto/SafeArrayGetIID
dev_langs:
- c++
req.header: oleauto.h
req.include-header: 
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- SafeArrayGetIID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SafeArrayGetIID function


## -description


Gets the GUID of the interface contained within the specified safe array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.



### -param pguid [out]

The GUID of the interface.


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
 



