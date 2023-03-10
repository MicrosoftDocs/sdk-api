---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.get_Name
title: ITPluggableTerminalSuperclassRegistration::get_Name (termmgr.h)
description: The get_Name method gets the friendly name for the terminal superclass.
helpviewer_keywords: ["ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","get_Name method","ITPluggableTerminalSuperclassRegistration.get_Name","ITPluggableTerminalSuperclassRegistration::get_Name","_tapi3_itpluggableterminalsuperclassregistration_get_name","get_Name","get_Name method [TAPI 2.2]","get_Name method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","tapi3.itpluggableterminalsuperclassregistration_get_name","termmgr/ITPluggableTerminalSuperclassRegistration::get_Name"]
old-location: tapi3\itpluggableterminalsuperclassregistration_get_name.htm
tech.root: tapi3
ms.assetid: 42f58ac2-4fda-436c-bbfd-d339296f736e
ms.date: 12/05/2018
ms.keywords: ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],get_Name method, ITPluggableTerminalSuperclassRegistration.get_Name, ITPluggableTerminalSuperclassRegistration::get_Name, _tapi3_itpluggableterminalsuperclassregistration_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, tapi3.itpluggableterminalsuperclassregistration_get_name, termmgr/ITPluggableTerminalSuperclassRegistration::get_Name
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
 - ITPluggableTerminalSuperclassRegistration::get_Name
 - termmgr/ITPluggableTerminalSuperclassRegistration::get_Name
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
 - ITPluggableTerminalSuperclassRegistration.get_Name
---

# ITPluggableTerminalSuperclassRegistration::get_Name


## -description

The 
<b>get_Name</b> method gets the friendly name for the terminal superclass.

## -parameters

### -param pName [out]

 Pointer to a <b>BSTR</b> representation of the friendly name. The <b>BSTR</b> is allocated using 
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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pName</i> parameter is not valid.

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



<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-put_name">put_Name</a>