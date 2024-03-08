---
UID: NF:tuner.ITuningSpace.put_UniqueName
title: ITuningSpace::put_UniqueName (tuner.h)
description: The put_UniqueName method sets a unique name for the tuning space.
helpviewer_keywords: ["ITuningSpace interface [Microsoft TV Technologies]","put_UniqueName method","ITuningSpace.put_UniqueName","ITuningSpace::put_UniqueName","ITuningSpaceput_UniqueName","mstv.ituningspace_put_uniquename","put_UniqueName","put_UniqueName method [Microsoft TV Technologies]","put_UniqueName method [Microsoft TV Technologies]","ITuningSpace interface","tuner/ITuningSpace::put_UniqueName"]
old-location: mstv\ituningspace_put_uniquename.htm
tech.root: mstv
ms.assetid: 44ce065b-5441-40c9-a987-6eafc04fba3d
ms.date: 12/05/2018
ms.keywords: ITuningSpace interface [Microsoft TV Technologies],put_UniqueName method, ITuningSpace.put_UniqueName, ITuningSpace::put_UniqueName, ITuningSpaceput_UniqueName, mstv.ituningspace_put_uniquename, put_UniqueName, put_UniqueName method [Microsoft TV Technologies], put_UniqueName method [Microsoft TV Technologies],ITuningSpace interface, tuner/ITuningSpace::put_UniqueName
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
 - ITuningSpace::put_UniqueName
 - tuner/ITuningSpace::put_UniqueName
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
 - ITuningSpace.put_UniqueName
---

# ITuningSpace::put_UniqueName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_UniqueName</b> method sets a unique name for the tuning space.

## -parameters

### -param Name [in]

Variable of type <b>BSTR</b> that specifies the unique name.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

If you attempt to add a new tuning space to the System Tuning Spaces collection, this property must be unique within the collection. For more information, see <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspacecontainer-add">ITuningSpaceContainer::Add</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ituningspace">ITuningSpace Interface</a>