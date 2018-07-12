---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.Delete
title: ITPluggableTerminalClassRegistration::Delete
author: windows-sdk-content
description: The Delete method deletes the terminal class from the registry.
old-location: tapi3\itpluggableterminalclassregistration_delete.htm
old-project: tapi
ms.assetid: ddc0e33a-d7f4-4380-b53b-e368f7646cbf
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: Delete, Delete method [TAPI 2.2], Delete method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],Delete method, ITPluggableTerminalClassRegistration.Delete, ITPluggableTerminalClassRegistration::Delete, _tapi3_itpluggableterminalclassregistration_delete, tapi3.itpluggableterminalclassregistration_delete, termmgr/ITPluggableTerminalClassRegistration::Delete
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TMGR_DIRECTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalClassRegistration.Delete
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalClassRegistration::Delete


## -description


The 
<b>Delete</b> method deletes the terminal class from the registry.


## -parameters




### -param bstrSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>



<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>
 

 

