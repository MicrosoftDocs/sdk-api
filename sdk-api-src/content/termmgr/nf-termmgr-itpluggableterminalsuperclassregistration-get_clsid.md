---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.get_CLSID
title: ITPluggableTerminalSuperclassRegistration::get_CLSID (termmgr.h)
description: The get_CLSID method gets the CLSID used to CoCreateInstance the terminal. (ITPluggableTerminalSuperclassRegistration.get_CLSID)
helpviewer_keywords: ["ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","get_CLSID method","ITPluggableTerminalSuperclassRegistration.get_CLSID","ITPluggableTerminalSuperclassRegistration::get_CLSID","_tapi3_itpluggableterminalsuperclassregistration_get_clsid","get_CLSID","get_CLSID method [TAPI 2.2]","get_CLSID method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","tapi3.itpluggableterminalsuperclassregistration_get_clsid","termmgr/ITPluggableTerminalSuperclassRegistration::get_CLSID"]
old-location: tapi3\itpluggableterminalsuperclassregistration_get_clsid.htm
tech.root: tapi3
ms.assetid: d343284c-ffe1-4491-8476-37bcdd6e1a97
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],get_CLSID method, ITPluggableTerminalSuperclassRegistration.get_CLSID, ITPluggableTerminalSuperclassRegistration::get_CLSID, _tapi3_itpluggableterminalsuperclassregistration_get_clsid, get_CLSID, get_CLSID method [TAPI 2.2], get_CLSID method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_get_clsid, termmgr/ITPluggableTerminalSuperclassRegistration::get_CLSID
req.header: termmgr.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITPluggableTerminalSuperclassRegistration::get_CLSID
 - termmgr/ITPluggableTerminalSuperclassRegistration::get_CLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalSuperclassRegistration.get_CLSID
---

# ITPluggableTerminalSuperclassRegistration::get_CLSID


## -description

The 
<b>get_CLSID</b> method gets the CLSID used to <b>CoCreateInstance</b> the terminal.

## -parameters

### -param pCLSID [out]

 The <b>BSTR</b> representation of the CLSID. The <b>BSTR</b> is allocated using 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a>. The <b>BSTR</b> argument should be deallocated by the client.

## -returns

This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCLSID</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalsuperclassregistration">ITPluggableTerminalSuperclassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-put_clsid">put_CLSID</a>
