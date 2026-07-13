---
UID: NF:bdatif.IBDA_TIF_REGISTRATION.UnregisterTIF
title: IBDA_TIF_REGISTRATION::UnregisterTIF (bdatif.h)
description: The UnregisterTIF method unregisters a Transport Information Filter (TIF) with the Network Provider.
helpviewer_keywords: ["IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies]","UnregisterTIF method","IBDA_TIF_REGISTRATION.UnregisterTIF","IBDA_TIF_REGISTRATION::UnregisterTIF","IBDA_TIF_REGISTRATIONUnregisterTIF","UnregisterTIF","UnregisterTIF method [Microsoft TV Technologies]","UnregisterTIF method [Microsoft TV Technologies]","IBDA_TIF_REGISTRATION interface","bdatif/IBDA_TIF_REGISTRATION::UnregisterTIF","mstv.ibda_tif_registration_unregistertif"]
old-location: mstv\ibda_tif_registration_unregistertif.htm
tech.root: mstv
ms.assetid: 6ba46145-6b77-4577-9611-0e0a155aa308
ms.date: 12/05/2018
ms.keywords: IBDA_TIF_REGISTRATION interface [Microsoft TV Technologies],UnregisterTIF method, IBDA_TIF_REGISTRATION.UnregisterTIF, IBDA_TIF_REGISTRATION::UnregisterTIF, IBDA_TIF_REGISTRATIONUnregisterTIF, UnregisterTIF, UnregisterTIF method [Microsoft TV Technologies], UnregisterTIF method [Microsoft TV Technologies],IBDA_TIF_REGISTRATION interface, bdatif/IBDA_TIF_REGISTRATION::UnregisterTIF, mstv.ibda_tif_registration_unregistertif
req.header: bdatif.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_TIF_REGISTRATION::UnregisterTIF
 - bdatif/IBDA_TIF_REGISTRATION::UnregisterTIF
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IBDA_TIF_REGISTRATION.UnregisterTIF
---

# IBDA_TIF_REGISTRATION::UnregisterTIF


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>UnregisterTIF</b> method unregisters a Transport Information Filter (TIF) with the Network Provider.

## -parameters

### -param pvRegistrationContext [in]

Specifies the token that the <b>RegisterTIFEx</b> method returned in the <i>ppvRegistrationContext</i> parameter.

## -returns

The method returns an <b>HRESULT</b> value.

## -see-also

<a href="/previous-versions/windows/desktop/api/bdatif/nn-bdatif-ibda_tif_registration">IBDA_TIF_REGISTRATION Interface</a>