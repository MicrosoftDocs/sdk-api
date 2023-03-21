---
UID: NF:wcsplugin.IGamutMapModelPlugIn.Initialize
title: IGamutMapModelPlugIn::Initialize (wcsplugin.h)
description: Initializes a gamut map model profile (GMMP) by using the specified source and destination gamut boundary descriptions and optional source and destination device model plug-ins.
helpviewer_keywords: ["IGamutMapModelPlugIn interface [Windows Color System]","Initialize method","IGamutMapModelPlugIn.Initialize","IGamutMapModelPlugIn::Initialize","Initialize","Initialize method [Windows Color System]","Initialize method [Windows Color System]","IGamutMapModelPlugIn interface","_color_IGamutMapModelPlugIn::Initialize","wcs.IGamutMapModelPlugIn_Initialize","wcsplugin/IGamutMapModelPlugIn::Initialize"]
old-location: wcs\IGamutMapModelPlugIn_Initialize.htm
tech.root: WCS
ms.assetid: 86fb0f6b-d293-44de-ad1d-724436403535
ms.date: 12/05/2018
ms.keywords: IGamutMapModelPlugIn interface [Windows Color System],Initialize method, IGamutMapModelPlugIn.Initialize, IGamutMapModelPlugIn::Initialize, Initialize, Initialize method [Windows Color System], Initialize method [Windows Color System],IGamutMapModelPlugIn interface, _color_IGamutMapModelPlugIn::Initialize, wcs.IGamutMapModelPlugIn_Initialize, wcsplugin/IGamutMapModelPlugIn::Initialize
req.header: wcsplugin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IGamutMapModelPlugIn::Initialize
 - wcsplugin/IGamutMapModelPlugIn::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IGamutMapModelPlugIn.Initialize
---

# IGamutMapModelPlugIn::Initialize


## -description

Initializes a gamut map model profile (GMMP) by using the specified source and destination gamut boundary descriptions and optional source and destination device model plug-ins.

## -parameters

### -param bstrXml [in]

A string that contains the BSTR XML GMMP profile. This is little-endian Unicode XML, but without the leading bytes to tag it as such. Also, the encoding keyword in the XML may not reflect this format.

### -param pSrcPlugIn [in]

A pointer to a source <a href="/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin">IDeviceModelPlugIn</a>. If <b>NULL</b>, it indicates the source device model profile is not a plug-in profile.

### -param pDestPlugIn [in]

A pointer to a destination <a href="/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin">IDeviceModelPlugIn</a>. If <b>NULL</b>, it indicates the destination device model profile is not a plug-in profile.

### -param pSrcGBD [in]

A pointer to a source <a href="/windows/desktop/api/wcsplugin/ns-wcsplugin-gamutboundarydescription">GamutBoundaryDescription</a>.

### -param pDestGBD [in]

A pointer to a destination <a href="/windows/desktop/api/wcsplugin/ns-wcsplugin-gamutboundarydescription">GamutBoundaryDescription</a>.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [IGamutMapModelPlugIn](/windows/win32/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)
