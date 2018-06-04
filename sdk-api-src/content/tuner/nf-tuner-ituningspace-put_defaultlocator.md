---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITuningSpace::put_DefaultLocator


## -description



The <b>put_DefaultLocator</b> method sets the default locator for this tuning space.




## -parameters




### -param LocatorVal






#### - pLocatorVal [in]

Pointer to the <a href="https://msdn.microsoft.com/1d6c18f0-e7f1-4a1c-9edb-e4b66297becf">ILocator</a> interface of the locator object.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



See <a href="https://msdn.microsoft.com/facc14bd-182e-4b8e-a567-1bf1d3c4ff36">ITuningSpace::get_DefaultLocator</a> for more information about the default locator.

For DVB tuning spaces, the sytem type (cable, terrestrial, or satelite) of the tuning space must match the locator object. Otherwise, the method returns DISP_E_TYPEMISMATCH. For more information, see <a href="https://msdn.microsoft.com/559f882a-4d1c-4fe1-af21-b3ad7ccd3ff2">IDVBTuningSpace::put_SystemType</a>.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

