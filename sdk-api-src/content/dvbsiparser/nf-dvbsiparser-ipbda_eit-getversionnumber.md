---
UID: NF:dvbsiparser.IPBDA_EIT.GetVersionNumber
title: IPBDA_EIT::GetVersionNumber (dvbsiparser.h)
description: Gets the version number from an event information table (EIT) in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetVersionNumber","GetVersionNumber method [Microsoft TV Technologies]","GetVersionNumber method [Microsoft TV Technologies]","IPBDA_EIT interface","IPBDA_EIT interface [Microsoft TV Technologies]","GetVersionNumber method","IPBDA_EIT.GetVersionNumber","IPBDA_EIT::GetVersionNumber","dvbsiparser/IPBDA_EIT::GetVersionNumber","mstv.ipbda_eit_getversionnumber"]
old-location: mstv\ipbda_eit_getversionnumber.htm
tech.root: mstv
ms.assetid: 16249557-f1e4-4a9f-93bd-b93a2bb72353
ms.date: 12/05/2018
ms.keywords: GetVersionNumber, GetVersionNumber method [Microsoft TV Technologies], GetVersionNumber method [Microsoft TV Technologies],IPBDA_EIT interface, IPBDA_EIT interface [Microsoft TV Technologies],GetVersionNumber method, IPBDA_EIT.GetVersionNumber, IPBDA_EIT::GetVersionNumber, dvbsiparser/IPBDA_EIT::GetVersionNumber, mstv.ipbda_eit_getversionnumber
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IPBDA_EIT::GetVersionNumber
 - dvbsiparser/IPBDA_EIT::GetVersionNumber
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IPBDA_EIT.GetVersionNumber
---

# IPBDA_EIT::GetVersionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the version number from an event information table (EIT) in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param pwVal [out]

Receives the version number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbda_eit">IPBDA_EIT</a>