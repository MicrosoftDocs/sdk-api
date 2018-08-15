---
UID: NF:tuner.ITuningSpaceContainer._TuningSpacesForCLSID
title: ITuningSpaceContainer::_TuningSpacesForCLSID
author: windows-sdk-content
description: The _TuningSpacesForCLSID method retrieves a collection of tuning spaces that match the specified CLSID.
old-location: mstv\ituningspacecontainer__tuningspacesforclsid.htm
old-project: mstv
ms.assetid: f31be8f8-3482-484a-b1a3-f27f3e0f7203
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],_TuningSpacesForCLSID method, ITuningSpaceContainer._TuningSpacesForCLSID, ITuningSpaceContainer::_TuningSpacesForCLSID, ITuningSpaceContainer_TuningSpacesForCLSID, _TuningSpacesForCLSID, _TuningSpacesForCLSID method [Microsoft TV Technologies], _TuningSpacesForCLSID method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer__tuningspacesforclsid, tuner/ITuningSpaceContainer::_TuningSpacesForCLSID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpaceContainer._TuningSpacesForCLSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

