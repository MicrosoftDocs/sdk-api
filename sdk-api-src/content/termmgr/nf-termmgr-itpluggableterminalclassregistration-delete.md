---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.Delete
title: ITPluggableTerminalClassRegistration::Delete (termmgr.h)
author: windows-sdk-content
description: The Delete method deletes the terminal class from the registry.
old-location: tapi3\itpluggableterminalclassregistration_delete.htm
tech.root: Tapi
ms.assetid: ddc0e33a-d7f4-4380-b53b-e368f7646cbf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [TAPI 2.2], Delete method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],Delete method, ITPluggableTerminalClassRegistration.Delete, ITPluggableTerminalClassRegistration::Delete, _tapi3_itpluggableterminalclassregistration_delete, tapi3.itpluggableterminalclassregistration_delete, termmgr/ITPluggableTerminalClassRegistration::Delete
ms.topic: method
f1_keywords: 
 - "termmgr/ITPluggableTerminalClassRegistration.Delete"
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
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nf-termmgr-itpluggableterminalclassregistration-add">Add</a>



<a href="https://docs.microsoft.com/windows/desktop/api/termmgr/nn-termmgr-itpluggableterminalclassregistration">ITPluggableTerminalClassRegistration</a>
 

 

