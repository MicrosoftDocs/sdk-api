---
UID: NN:gpmgmt.IGPMWMIFilter
title: IGPMWMIFilter (gpmgmt.h)
description: The IGPMWMIFilter interface contains methods that allow you to set and retrieve security attributes and various properties for a WMI filter. WMI filter queries are specified using WMI Query Language (WQL).
helpviewer_keywords: ["GPMWMIFilter","IGPMWMIFilter","IGPMWMIFilter interface [GPMC]","IGPMWMIFilter interface [GPMC]","described","_win32_igpmwmifilter","gpmc.igpmwmifilter","gpmgmt/IGPMWMIFilter"]
old-location: gpmc\igpmwmifilter.htm
tech.root: gpmc
ms.assetid: 801428f1-9ce5-4348-acab-23cc9ea8cac3
ms.date: 12/05/2018
ms.keywords: GPMWMIFilter, IGPMWMIFilter, IGPMWMIFilter interface [GPMC], IGPMWMIFilter interface [GPMC],described, _win32_igpmwmifilter, gpmc.igpmwmifilter, gpmgmt/IGPMWMIFilter
req.header: gpmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Gpmgmt.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Gpmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGPMWMIFilter
 - gpmgmt/IGPMWMIFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpmgmt.dll
api_name:
 - IGPMWMIFilter
 - GPMWMIFilter
---

# IGPMWMIFilter interface


## -description

The 
<b>IGPMWMIFilter</b> interface contains methods that allow you to set and retrieve security attributes and various properties for a WMI filter. WMI filter queries are specified using WMI Query Language (WQL).

## -inheritance

The <b>IGPMWMIFilter</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IGPMWMIFilter</b> also has these types of members:

## -remarks

For information about importing, exporting, and copying WMI filters, see the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getobjecttext">IWbemClassObject::GetObjectText</a> and 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-imofcompiler-compilebuffer">IMofCompiler::CompileBuffer</a> methods in the WMI SDK.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpm">IGPM</a>



<a href="/previous-versions/windows/desktop/api/gpmgmt/nn-gpmgmt-igpmwmifiltercollection">IGPMWMIFilterCollection</a>
