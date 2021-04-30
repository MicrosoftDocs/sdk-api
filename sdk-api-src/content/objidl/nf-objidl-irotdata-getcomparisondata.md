---
UID: NF:objidl.IROTData.GetComparisonData
title: IROTData::GetComparisonData (objidl.h)
description: Retrieves data from a moniker that can be used to test the moniker for equality against another moniker.
helpviewer_keywords: ["GetComparisonData","GetComparisonData method [COM]","GetComparisonData method [COM]","IROTData interface","IROTData interface [COM]","GetComparisonData method","IROTData.GetComparisonData","IROTData::GetComparisonData","_com_irotdata_getcomparisondata","com.irotdata_getcomparisondata","objidl/IROTData::GetComparisonData"]
old-location: com\irotdata_getcomparisondata.htm
tech.root: com
ms.assetid: e7f2d3a6-2517-47bc-aa6a-509d72881a0b
ms.date: 12/05/2018
ms.keywords: GetComparisonData, GetComparisonData method [COM], GetComparisonData method [COM],IROTData interface, IROTData interface [COM],GetComparisonData method, IROTData.GetComparisonData, IROTData::GetComparisonData, _com_irotdata_getcomparisondata, com.irotdata_getcomparisondata, objidl/IROTData::GetComparisonData
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IROTData::GetComparisonData
 - objidl/IROTData::GetComparisonData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
api_name:
 - IROTData.GetComparisonData
---

# IROTData::GetComparisonData


## -description

Retrieves data from a moniker that can be used to test the moniker for equality against another moniker.

## -parameters

### -param pbData [out]

A pointer to a buffer that receives the comparison data.

### -param cbMax [in]

The length of the buffer specified in <i>pbData</i>.

### -param pcbData [out]

A pointer to a variable that receives the length of the comparison data.

## -returns

This method can return the standard return values E_OUTOFMEMORY and S_OK.

## -remarks

The <b>GetComparisonData</b> method is primarily called by the running object table (ROT). The comparison data returned by the method is tested for binary equality against the comparison data returned by another moniker. The <i>pcbData</i> parameter enables the ROT to locate the end of the data retrieved.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
The comparison data that you return must uniquely identify the moniker, while still being as short as possible. The comparison data should include information about the internal state of the moniker, as well as the moniker's CLSID. For example, the comparison data for a file moniker would include the path name stored within the moniker, as well as the CLSID of the file moniker implementation. This makes it possible to distinguish two monikers that happen to store similar state information but are instances of different moniker classes.

The comparison data for a moniker cannot exceed 2048 bytes in length. For composite monikers, the total length of the comparison data for all of its components cannot exceed 2048 bytes; consequently, if your moniker can be a component within a composite moniker, the comparison data you return must be significantly less than 2048 bytes.

If your comparison data is longer than the value specified by the <i>cbMax</i> parameter, you must return an error. Note that when <b>GetComparisonData</b> is called on the components of a composite moniker, the value of <i>cbMax</i> becomes smaller for each moniker in sequence.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irotdata">IROTData</a>