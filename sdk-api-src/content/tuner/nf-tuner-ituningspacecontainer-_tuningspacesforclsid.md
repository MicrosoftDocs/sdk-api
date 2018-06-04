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

# ITuningSpaceContainer::_TuningSpacesForCLSID


## -description



The <b>_TuningSpacesForCLSID</b> method retrieves a collection of tuning spaces that match the specified CLSID.




## -parameters




### -param SpaceCLSID [in]

Specifies the CLSID of the tuning spaces to retrieve.


### -param NewColl






#### - ppTuningSpaces [out]

Address of a variable that receives an <a href="https://msdn.microsoft.com/db252e22-8efe-4bfc-8fd3-2be7022bbbbd">ITuningSpaces</a> interface pointer. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The CLSID represents the object that implements the tuning space. The same object may implement several related tuning spaces. For example, ATSC Digital Antenna and ATSC Digital Cable are both supported by the <a href="https://msdn.microsoft.com/8535a8c3-35df-4c6c-872a-437f5c7a2e56">ATSCTuningSpace</a> object (CLSID_ATSCTuningSpace).

This method matches against the CLSID returned by the <a href="https://msdn.microsoft.com/def4aac2-3d0b-4ce6-9f6b-d13e7c3cc86d">ITuningSpace::get_CLSID</a> method. The returned collection might be empty; call <a href="https://msdn.microsoft.com/df620224-5ee4-4cb6-973a-560dc9d9f4de">ITuningSpaces::get_Count</a> to determine how many tuning spaces were returned.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

