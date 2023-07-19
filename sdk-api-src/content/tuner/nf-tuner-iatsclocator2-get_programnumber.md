---
UID: NF:tuner.IATSCLocator2.get_ProgramNumber
title: IATSCLocator2::get_ProgramNumber (tuner.h)
description: The get_ProgramNumber method retrieves the program number.
helpviewer_keywords: ["IATSCLocator2 interface [Microsoft TV Technologies]","get_ProgramNumber method","IATSCLocator2.get_ProgramNumber","IATSCLocator2::get_ProgramNumber","IATSCLocator2get_ProgramNumber","get_ProgramNumber","get_ProgramNumber method [Microsoft TV Technologies]","get_ProgramNumber method [Microsoft TV Technologies]","IATSCLocator2 interface","mstv.iatsclocator2_get_programnumber","tuner/IATSCLocator2::get_ProgramNumber"]
old-location: mstv\iatsclocator2_get_programnumber.htm
tech.root: mstv
ms.assetid: 66f92cb0-a89e-4c34-8995-a94eb1bc33dc
ms.date: 12/05/2018
ms.keywords: IATSCLocator2 interface [Microsoft TV Technologies],get_ProgramNumber method, IATSCLocator2.get_ProgramNumber, IATSCLocator2::get_ProgramNumber, IATSCLocator2get_ProgramNumber, get_ProgramNumber, get_ProgramNumber method [Microsoft TV Technologies], get_ProgramNumber method [Microsoft TV Technologies],IATSCLocator2 interface, mstv.iatsclocator2_get_programnumber, tuner/IATSCLocator2::get_ProgramNumber
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - IATSCLocator2::get_ProgramNumber
 - tuner/IATSCLocator2::get_ProgramNumber
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
 - IATSCLocator2.get_ProgramNumber
---

# IATSCLocator2::get_ProgramNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_ProgramNumber</b> method retrieves the program number.

## -parameters

### -param ProgramNumber [out]

Pointer to a variable that receives the program number.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-iatsclocator2">IATSCLocator2 Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-iatsclocator2-put_programnumber">put_ProgramNumber</a>