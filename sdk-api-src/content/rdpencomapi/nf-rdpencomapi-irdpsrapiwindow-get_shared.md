---
UID: NF:rdpencomapi.IRDPSRAPIWindow.get_Shared
title: IRDPSRAPIWindow::get_Shared (rdpencomapi.h)
description: Gets or sets the sharing property for a window. (Get)
helpviewer_keywords: ["IRDPSRAPIWindow interface [RDP]","Shared property","IRDPSRAPIWindow.Shared","IRDPSRAPIWindow.get_Shared","IRDPSRAPIWindow::Shared","IRDPSRAPIWindow::get_Shared","IRDPSRAPIWindow::put_Shared","RDPSRAPIWindow object [RDP]","Shared property","Shared property [RDP]","Shared property [RDP]","IRDPSRAPIWindow interface","Shared property [RDP]","RDPSRAPIWindow object","get_Shared","rdp.irdpsrapiwindow_shared","rdpencomapi/IRDPSRAPIWindow::Shared","rdpencomapi/IRDPSRAPIWindow::get_Shared","rdpencomapi/IRDPSRAPIWindow::put_Shared"]
old-location: rdp\irdpsrapiwindow_shared.htm
tech.root: rdp
ms.assetid: e07ebdbc-79ce-4a85-9960-197c4c7ca445
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIWindow interface [RDP],Shared property, IRDPSRAPIWindow.Shared, IRDPSRAPIWindow.get_Shared, IRDPSRAPIWindow::Shared, IRDPSRAPIWindow::get_Shared, IRDPSRAPIWindow::put_Shared, RDPSRAPIWindow object [RDP],Shared property, Shared property [RDP], Shared property [RDP],IRDPSRAPIWindow interface, Shared property [RDP],RDPSRAPIWindow object, get_Shared, rdp.irdpsrapiwindow_shared, rdpencomapi/IRDPSRAPIWindow::Shared, rdpencomapi/IRDPSRAPIWindow::get_Shared, rdpencomapi/IRDPSRAPIWindow::put_Shared
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
 - IRDPSRAPIWindow::get_Shared
 - rdpencomapi/IRDPSRAPIWindow::get_Shared
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
 - IRDPSRAPIWindow.Shared
 - IRDPSRAPIWindow.get_Shared
 - IRDPSRAPIWindow.put_Shared
 - RDPSRAPIWindow.Shared
---

# IRDPSRAPIWindow::get_Shared


## -description

Gets or sets the sharing property for a window.

Whether a window is  shared or not also depends on the state of the parent application object and on the enabled state of the sharing filter. For more information about the enabled state of the sharing filter, see  <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiapplicationfilter-get_enabled">Enabled Property of IRDPSRAPIApplicationFilter</a>.

This property is read/write.

## -parameters

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiwindow">IRDPSRAPIWindow</a>
