---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.put_Name
title: ITPluggableTerminalSuperclassRegistration::put_Name (termmgr.h)
description: The put_Name method sets the friendly name for the terminal superclass.
helpviewer_keywords: ["ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","put_Name method","ITPluggableTerminalSuperclassRegistration.put_Name","ITPluggableTerminalSuperclassRegistration::put_Name","_tapi3_itpluggableterminalsuperclassregistration_put_name","put_Name","put_Name method [TAPI 2.2]","put_Name method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","tapi3.itpluggableterminalsuperclassregistration_put_name","termmgr/ITPluggableTerminalSuperclassRegistration::put_Name"]
old-location: tapi3\itpluggableterminalsuperclassregistration_put_name.htm
tech.root: tapi3
ms.assetid: fe9b569b-bfb7-401b-98a8-5db7f3739d41
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],put_Name method, ITPluggableTerminalSuperclassRegistration.put_Name, ITPluggableTerminalSuperclassRegistration::put_Name, _tapi3_itpluggableterminalsuperclassregistration_put_name, put_Name, put_Name method [TAPI 2.2], put_Name method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_put_name, termmgr/ITPluggableTerminalSuperclassRegistration::put_Name
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
 - ITPluggableTerminalSuperclassRegistration::put_Name
 - termmgr/ITPluggableTerminalSuperclassRegistration::put_Name
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
 - ITPluggableTerminalSuperclassRegistration.put_Name
---

# ITPluggableTerminalSuperclassRegistration::put_Name


## -description

The 
<b>put_Name</b> method sets the friendly name for the terminal superclass.

## -parameters

### -param bstrName [in]

The <b>BSTR</b> representation of the friendly name.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>bstrName</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalsuperclassregistration">ITPluggableTerminalSuperclassRegistration</a>



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-get_name">get_Name</a>