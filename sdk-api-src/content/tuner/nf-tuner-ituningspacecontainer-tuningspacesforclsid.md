---
UID: NF:tuner.ITuningSpaceContainer.TuningSpacesForCLSID
title: ITuningSpaceContainer::TuningSpacesForCLSID (tuner.h)
description: The TuningSpacesForCLSID method retrieves a collection of tuning spaces that match the specified CLSID.This method is intended for Automation clients, because it returns the CLSID as a BSTR.
old-location: mstv\ituningspacecontainer_tuningspacesforclsid.htm
tech.root: mstv
ms.assetid: 8e2d6103-baed-40ee-9a94-9434cf8e3474
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],TuningSpacesForCLSID method, ITuningSpaceContainer.TuningSpacesForCLSID, ITuningSpaceContainer::TuningSpacesForCLSID, TuningSpacesForCLSID, TuningSpacesForCLSID method [Microsoft TV Technologies], TuningSpacesForCLSID method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer_tuningspacesforclsid, tuner/ITuningSpaceContainer::TuningSpacesForCLSID
f1_keywords:
- tuner/ITuningSpaceContainer.TuningSpacesForCLSID
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- ITuningSpaceContainer.TuningSpacesForCLSID
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuningSpaceContainer::TuningSpacesForCLSID


## -description



The <b>TuningSpacesForCLSID</b> method retrieves a collection of tuning spaces that match the specified CLSID.

This method is intended for Automation clients, because it returns the CLSID as a <b>BSTR</b>. C++ applications can use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-tuningspacesforclsid">ITuningSpaceContainer::_TuningSpacesForCLSID</a> method instead, which returns a GUID value.






## -parameters




### -param SpaceCLSID [in]

String representation of the CLSID of the tuning space.


### -param NewColl [out]

Receives a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspaces">ITuningSpaces</a> interface. The caller must release the interface.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>
 

 

