---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.put_CLSID
title: ITPluggableTerminalSuperclassRegistration::put_CLSID (termmgr.h)
description: The put_CLSID method sets the CLSID used to CoCreateInstance the terminal. (ITPluggableTerminalSuperclassRegistration.put_CLSID)
helpviewer_keywords: ["ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","put_CLSID method","ITPluggableTerminalSuperclassRegistration.put_CLSID","ITPluggableTerminalSuperclassRegistration::put_CLSID","_tapi3_itpluggableterminalsuperclassregistration_put_clsid","put_CLSID","put_CLSID method [TAPI 2.2]","put_CLSID method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","tapi3.itpluggableterminalsuperclassregistration_put_clsid","termmgr/ITPluggableTerminalSuperclassRegistration::put_CLSID"]
old-location: tapi3\itpluggableterminalsuperclassregistration_put_clsid.htm
tech.root: tapi3
ms.assetid: ccb7159d-e838-408b-9565-a9854c4ba592
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],put_CLSID method, ITPluggableTerminalSuperclassRegistration.put_CLSID, ITPluggableTerminalSuperclassRegistration::put_CLSID, _tapi3_itpluggableterminalsuperclassregistration_put_clsid, put_CLSID, put_CLSID method [TAPI 2.2], put_CLSID method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_put_clsid, termmgr/ITPluggableTerminalSuperclassRegistration::put_CLSID
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
 - ITPluggableTerminalSuperclassRegistration::put_CLSID
 - termmgr/ITPluggableTerminalSuperclassRegistration::put_CLSID
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
 - ITPluggableTerminalSuperclassRegistration.put_CLSID
---

# ITPluggableTerminalSuperclassRegistration::put_CLSID


## -description

The 
<b>put_CLSID</b> method sets the CLSID used to <b>CoCreateInstance</b> the terminal.

## -parameters

### -param bstrCLSID [in]

The <b>BSTR</b> representation of the CLSID.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>bstrCLSID</i> parameter is not valid.

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
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalsuperclassregistration">ITPluggableTerminalSuperclassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-get_clsid">get_CLSID</a>
