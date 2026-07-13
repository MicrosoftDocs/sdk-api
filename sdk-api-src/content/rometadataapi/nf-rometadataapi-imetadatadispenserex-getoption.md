---
UID: NF:rometadataapi.IMetaDataDispenserEx.GetOption
title: IMetaDataDispenserEx::GetOption (rometadataapi.h)
description: Gets the value of the specified option for the current metadata scope. The option controls how calls to the current metadata scope are handled.
helpviewer_keywords: ["GetOption","GetOption method [Windows Runtime]","GetOption method [Windows Runtime]","IMetaDataDispenserEx interface","IMetaDataDispenserEx interface [Windows Runtime]","GetOption method","IMetaDataDispenserEx.GetOption","IMetaDataDispenserEx::GetOption","rometadataapi/IMetaDataDispenserEx::GetOption","winrt.imetadatadispenserex_getoption"]
old-location: winrt\imetadatadispenserex_getoption.htm
tech.root: WinRT
ms.assetid: 862948bd-6fce-4af9-9c68-1d3291e13053
ms.date: 12/05/2018
ms.keywords: GetOption, GetOption method [Windows Runtime], GetOption method [Windows Runtime],IMetaDataDispenserEx interface, IMetaDataDispenserEx interface [Windows Runtime],GetOption method, IMetaDataDispenserEx.GetOption, IMetaDataDispenserEx::GetOption, rometadataapi/IMetaDataDispenserEx::GetOption, winrt.imetadatadispenserex_getoption
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - IMetaDataDispenserEx::GetOption
 - rometadataapi/IMetaDataDispenserEx::GetOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx.GetOption
---

# IMetaDataDispenserEx::GetOption


## -description

Gets the value of the specified option for the current metadata scope. The option controls how calls to the current metadata scope are handled.

## -parameters

### -param optionId [in]

A pointer to a GUID that specifies the option to be retrieved. See the Remarks section for a list of supported GUIDs.

### -param pValue [out]

The value of the returned option. The type of this value will be a variant of the specified option's type.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following list shows the GUIDs that are supported for this method. For descriptions, see the <a href="/windows/desktop/api/rometadataapi/nf-rometadataapi-imetadatadispenserex-setoption">SetOption</a> method. If <i>optionId</i> is not in this list, this method returns HRESULT <b>E_INVALIDARG</b>, indicating an incorrect parameter.

<ul>
<li>
MetaDataCheckDuplicatesFor

</li>
<li>
MetaDataRefToDefCheck

</li>
<li>
MetaDataNotificationForTokenMovement

</li>
<li>
MetaDataSetENC

</li>
<li>
MetaDataErrorIfEmitOutOfOrder

</li>
<li>
MetaDataGenerateTCEAdapters

</li>
<li>
MetaDataLinkerOptions

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenserex">IMetaDataDispenserEx</a>