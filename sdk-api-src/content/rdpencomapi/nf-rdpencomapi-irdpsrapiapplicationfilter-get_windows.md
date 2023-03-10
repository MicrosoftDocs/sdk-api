---
UID: NF:rdpencomapi.IRDPSRAPIApplicationFilter.get_Windows
title: IRDPSRAPIApplicationFilter::get_Windows (rdpencomapi.h)
description: The list of sharable windows.
helpviewer_keywords: ["IRDPSRAPIApplicationFilter interface [RDP]","Windows property","IRDPSRAPIApplicationFilter.Windows","IRDPSRAPIApplicationFilter.get_Windows","IRDPSRAPIApplicationFilter::Windows","IRDPSRAPIApplicationFilter::get_Windows","RDPSRAPIApplicationFilter object [RDP]","Windows property","Windows property [RDP]","Windows property [RDP]","IRDPSRAPIApplicationFilter interface","Windows property [RDP]","RDPSRAPIApplicationFilter object","get_Windows","rdp.irdpsrapiapplicationfilter_windows","rdpencomapi/IRDPSRAPIApplicationFilter::Windows","rdpencomapi/IRDPSRAPIApplicationFilter::get_Windows"]
old-location: rdp\irdpsrapiapplicationfilter_windows.htm
tech.root: rdp
ms.assetid: cc964964-0f3a-410c-b1f4-426abd9c1a22
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIApplicationFilter interface [RDP],Windows property, IRDPSRAPIApplicationFilter.Windows, IRDPSRAPIApplicationFilter.get_Windows, IRDPSRAPIApplicationFilter::Windows, IRDPSRAPIApplicationFilter::get_Windows, RDPSRAPIApplicationFilter object [RDP],Windows property, Windows property [RDP], Windows property [RDP],IRDPSRAPIApplicationFilter interface, Windows property [RDP],RDPSRAPIApplicationFilter object, get_Windows, rdp.irdpsrapiapplicationfilter_windows, rdpencomapi/IRDPSRAPIApplicationFilter::Windows, rdpencomapi/IRDPSRAPIApplicationFilter::get_Windows
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPIApplicationFilter::get_Windows
 - rdpencomapi/IRDPSRAPIApplicationFilter::get_Windows
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIApplicationFilter.Windows
 - IRDPSRAPIApplicationFilter.get_Windows
 - RDPSRAPIApplicationFilter.Windows
---

# IRDPSRAPIApplicationFilter::get_Windows


## -description

The list of sharable windows.

This property is read-only.

## -parameters

## -remarks

The window objects are also available through the list returned by <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiapplication-get_windows">IRDPSRAPIApplication::Windows</a>. The windows are also exposed by the application filter because it provides easy access to all windows in the session, especially for applications that share only at the window level.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiapplicationfilter">IRDPSRAPIApplicationFilter</a>