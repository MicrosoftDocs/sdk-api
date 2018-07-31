---
UID: NF:tuner.ITuningSpaceContainer.TuningSpacesForCLSID
title: ITuningSpaceContainer::TuningSpacesForCLSID
author: windows-sdk-content
description: The TuningSpacesForCLSID method retrieves a collection of tuning spaces that match the specified CLSID.This method is intended for Automation clients, because it returns the CLSID as a BSTR.
old-location: mstv\ituningspacecontainer_tuningspacesforclsid.htm
old-project: mstv
ms.assetid: 8e2d6103-baed-40ee-9a94-9434cf8e3474
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],TuningSpacesForCLSID method, ITuningSpaceContainer.TuningSpacesForCLSID, ITuningSpaceContainer::TuningSpacesForCLSID, TuningSpacesForCLSID, TuningSpacesForCLSID method [Microsoft TV Technologies], TuningSpacesForCLSID method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_tuningspacesforclsid, tuner/ITuningSpaceContainer::TuningSpacesForCLSID
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tuner.h
req.include-header: 
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
 - ITuningSpaceContainer.TuningSpacesForCLSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITuningSpaceContainer::TuningSpacesForCLSID


## -description



The <b>TuningSpacesForCLSID</b> method retrieves a collection of tuning spaces that match the specified CLSID.

This method is intended for Automation clients, because it returns the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="https://msdn.microsoft.com/f31be8f8-3482-484a-b1a3-f27f3e0f7203">ITuningSpaceContainer::_TuningSpacesForCLSID</a> method instead, which returns a GUID value.






## -parameters




### -param SpaceCLSID [in]

String representation of the CLSID of the tuning space.


### -param NewColl






#### - ppTuningSpaces [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/db252e22-8efe-4bfc-8fd3-2be7022bbbbd">ITuningSpaces</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/8f053c53-2a2b-4d98-a510-c516faa21611">ITuningSpaceContainer Interface</a>
 

 

