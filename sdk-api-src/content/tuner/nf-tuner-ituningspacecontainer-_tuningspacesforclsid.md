---
UID: NF:tuner.ITuningSpaceContainer._TuningSpacesForCLSID
title: ITuningSpaceContainer::_TuningSpacesForCLSID (tuner.h)
description: The _TuningSpacesForCLSID method retrieves a collection of tuning spaces that match the specified CLSID.
helpviewer_keywords: ["ITuningSpaceContainer interface [Microsoft TV Technologies]","_TuningSpacesForCLSID method","ITuningSpaceContainer._TuningSpacesForCLSID","ITuningSpaceContainer::_TuningSpacesForCLSID","ITuningSpaceContainer_TuningSpacesForCLSID","_TuningSpacesForCLSID","_TuningSpacesForCLSID method [Microsoft TV Technologies]","_TuningSpacesForCLSID method [Microsoft TV Technologies]","ITuningSpaceContainer interface","mstv.ituningspacecontainer__tuningspacesforclsid","tuner/ITuningSpaceContainer::_TuningSpacesForCLSID"]
old-location: mstv\ituningspacecontainer__tuningspacesforclsid.htm
tech.root: mstv
ms.assetid: f31be8f8-3482-484a-b1a3-f27f3e0f7203
ms.date: 12/05/2018
ms.keywords: ITuningSpaceContainer interface [Microsoft TV Technologies],_TuningSpacesForCLSID method, ITuningSpaceContainer._TuningSpacesForCLSID, ITuningSpaceContainer::_TuningSpacesForCLSID, ITuningSpaceContainer_TuningSpacesForCLSID, _TuningSpacesForCLSID, _TuningSpacesForCLSID method [Microsoft TV Technologies], _TuningSpacesForCLSID method [Microsoft TV Technologies],ITuningSpaceContainer interface, mstv.ituningspacecontainer__tuningspacesforclsid, tuner/ITuningSpaceContainer::_TuningSpacesForCLSID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITuningSpaceContainer::_TuningSpacesForCLSID
 - tuner/ITuningSpaceContainer::_TuningSpacesForCLSID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ITuningSpaceContainer._TuningSpacesForCLSID
---

# ITuningSpaceContainer::_TuningSpacesForCLSID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>_TuningSpacesForCLSID</b> method retrieves a collection of tuning spaces that match the specified CLSID.

## -parameters

### -param SpaceCLSID [in]

Specifies the CLSID of the tuning spaces to retrieve.

### -param NewColl [out]

Address of a variable that receives an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspaces">ITuningSpaces</a> interface pointer. The caller must release the interface.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The CLSID represents the object that implements the tuning space. The same object may implement several related tuning spaces. For example, ATSC Digital Antenna and ATSC Digital Cable are both supported by the <a href="/previous-versions/windows/desktop/mstv/atsctuningspace-object">ATSCTuningSpace</a> object (CLSID_ATSCTuningSpace).

This method matches against the CLSID returned by the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_clsid">ITuningSpace::get_CLSID</a> method. The returned collection might be empty; call <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspaces-get_count">ITuningSpaces::get_Count</a> to determine how many tuning spaces were returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspacecontainer">ITuningSpaceContainer Interface</a>