---
UID: NF:vpconfig.IVPBaseConfig.SetConnectInfo
title: IVPBaseConfig::SetConnectInfo (vpconfig.h)
description: The SetConnectInfo method sets the video port connection parameters.
helpviewer_keywords: ["IVPBaseConfig interface [DirectShow]","SetConnectInfo method","IVPBaseConfig.SetConnectInfo","IVPBaseConfig::SetConnectInfo","IVPBaseConfigSetConnectInfo","SetConnectInfo","SetConnectInfo method [DirectShow]","SetConnectInfo method [DirectShow]","IVPBaseConfig interface","dshow.ivpbaseconfig_setconnectinfo","vpconfig/IVPBaseConfig::SetConnectInfo"]
old-location: dshow\ivpbaseconfig_setconnectinfo.htm
tech.root: dshow
ms.assetid: e52bb213-e6e7-4bae-9e1e-6b34f34cf1d1
ms.date: 12/05/2018
ms.keywords: IVPBaseConfig interface [DirectShow],SetConnectInfo method, IVPBaseConfig.SetConnectInfo, IVPBaseConfig::SetConnectInfo, IVPBaseConfigSetConnectInfo, SetConnectInfo, SetConnectInfo method [DirectShow], SetConnectInfo method [DirectShow],IVPBaseConfig interface, dshow.ivpbaseconfig_setconnectinfo, vpconfig/IVPBaseConfig::SetConnectInfo
req.header: vpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IVPBaseConfig::SetConnectInfo
 - vpconfig/IVPBaseConfig::SetConnectInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Vpconfig.h
api_name:
 - IVPBaseConfig.SetConnectInfo
---

# IVPBaseConfig::SetConnectInfo


## -description

The <code>SetConnectInfo</code> method sets the video port connection parameters.

## -parameters

### -param dwChosenEntry [in]

Specifies the index of connect information to pass to the driver. The value is a zero-based index into the array returned by the <a href="/windows/desktop/api/vpconfig/nf-vpconfig-ivpbaseconfig-getconnectinfo">IVPBaseConfig::GetConnectInfo</a> method.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

Include Dvp.h and Vptype.h before Vpconfig.h.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/vpconfig/nn-vpconfig-ivpbaseconfig">IVPBaseConfig Interface</a>