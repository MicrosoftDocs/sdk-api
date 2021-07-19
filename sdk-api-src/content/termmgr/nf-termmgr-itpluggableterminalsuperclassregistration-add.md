---
UID: NF:termmgr.ITPluggableTerminalSuperclassRegistration.Add
title: ITPluggableTerminalSuperclassRegistration::Add (termmgr.h)
description: The Add method adds a pluggable terminal superclass to the registry. If the superclass already exists, the method modifies the information for the superclass.
helpviewer_keywords: ["Add","Add method [TAPI 2.2]","Add method [TAPI 2.2]","ITPluggableTerminalSuperclassRegistration interface","ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2]","Add method","ITPluggableTerminalSuperclassRegistration.Add","ITPluggableTerminalSuperclassRegistration::Add","_tapi3_itpluggableterminalsuperclassregistration_add","tapi3.itpluggableterminalsuperclassregistration_add","termmgr/ITPluggableTerminalSuperclassRegistration::Add"]
old-location: tapi3\itpluggableterminalsuperclassregistration_add.htm
tech.root: tapi3
ms.assetid: ffef0255-c262-43d4-905f-5574c205c37e
ms.date: 12/05/2018
ms.keywords: Add, Add method [TAPI 2.2], Add method [TAPI 2.2],ITPluggableTerminalSuperclassRegistration interface, ITPluggableTerminalSuperclassRegistration interface [TAPI 2.2],Add method, ITPluggableTerminalSuperclassRegistration.Add, ITPluggableTerminalSuperclassRegistration::Add, _tapi3_itpluggableterminalsuperclassregistration_add, tapi3.itpluggableterminalsuperclassregistration_add, termmgr/ITPluggableTerminalSuperclassRegistration::Add
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
 - ITPluggableTerminalSuperclassRegistration::Add
 - termmgr/ITPluggableTerminalSuperclassRegistration::Add
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
 - ITPluggableTerminalSuperclassRegistration.Add
---

# ITPluggableTerminalSuperclassRegistration::Add


## -description

The 
<b>Add</b> method adds a pluggable terminal superclass to the registry. If the superclass already exists, the method modifies the information for the superclass.



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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Method failed.

</td>
</tr>
</table>

## -remarks

The 
<b>Add</b> method adds a new terminal superclass if the CLSID does not exist as an entry in the registry. The method modifies the information about a terminal superclass if the CLSID already exists in the registry.

If the CLSID for the terminal superclass was not set for terminal superclass, the 
<b>Add</b> method fails.

## -see-also

<a href="/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalsuperclassregistration-delete">Delete</a>



<a href="/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalsuperclassregistration">ITPluggableTerminalSuperclassRegistration</a>
