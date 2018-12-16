---
UID: NF:termmgr.ITPluggableTerminalClassRegistration.Add
title: ITPluggableTerminalClassRegistration::Add
author: windows-sdk-content
description: The Add method adds terminal information to the registry. If an entry for the terminal already exists, the method edits the entry.
old-location: tapi3\itpluggableterminalclassregistration_add.htm
tech.root: tapi
ms.assetid: 2e5104e1-5276-4c5b-9a1a-404904432982
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Add, Add method [TAPI 2.2], Add method [TAPI 2.2],ITPluggableTerminalClassRegistration interface, ITPluggableTerminalClassRegistration interface [TAPI 2.2],Add method, ITPluggableTerminalClassRegistration.Add, ITPluggableTerminalClassRegistration::Add, _tapi3_itpluggableterminalclassregistration_add, tapi3.itpluggableterminalclassregistration_add, termmgr/ITPluggableTerminalClassRegistration::Add
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
 - ITPluggableTerminalClassRegistration.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITPluggableTerminalClassRegistration::Add


## -description


The 
<b>Add</b> method adds terminal information to the registry. If an entry for the terminal already exists, the method edits the entry.


## -parameters




### -param bstrSuperclass [in]

The <b>BSTR</b> representation of the CLSID for the terminal superclass.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ddc0e33a-d7f4-4380-b53b-e368f7646cbf">Delete</a>



<a href="https://msdn.microsoft.com/178824f5-9dda-4e8a-b921-f2c9d064a83c">ITPluggableTerminalClassRegistration</a>
 

 

