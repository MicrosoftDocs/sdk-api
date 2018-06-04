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

# ITuningSpace::get_CLSID


## -description



The <b>get_CLSID</b> method gets the CLSID of the tuning space as a <b>BSTR</b>.




## -parameters




### -param SpaceCLSID






#### - pSpaceCLSID [out]

Pointer to a variable that receives a string representation of the tuning space CLSID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



This method provides script access to the <b>IPersist::GetClassID</b> method.

The returned CLSID represents the COM object that implements this tuning space. The CLSID is not guaranteed to be unique to this tuning space, however, because the same object may implement several tuning spaces.




## -see-also




<a href="https://msdn.microsoft.com/51850105-b3b1-4758-acde-05ca2f3439f2">ITuningSpace Interface</a>
 

 

