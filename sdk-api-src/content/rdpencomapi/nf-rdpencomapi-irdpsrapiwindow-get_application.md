---
UID: NF:rdpencomapi.IRDPSRAPIWindow.get_Application
title: IRDPSRAPIWindow::get_Application (rdpencomapi.h)
description: Returns a pointer to the application object that the window belongs to.
helpviewer_keywords: ["Application property [RDP]","Application property [RDP]","IRDPSRAPIWindow interface","Application property [RDP]","RDPSRAPIWindow object","IRDPSRAPIWindow interface [RDP]","Application property","IRDPSRAPIWindow.Application","IRDPSRAPIWindow.get_Application","IRDPSRAPIWindow::Application","IRDPSRAPIWindow::get_Application","RDPSRAPIWindow object [RDP]","Application property","get_Application","rdp.irdpsrapiwindow_application","rdpencomapi/IRDPSRAPIWindow::Application","rdpencomapi/IRDPSRAPIWindow::get_Application"]
old-location: rdp\irdpsrapiwindow_application.htm
tech.root: rdp
ms.assetid: a9c30288-c471-459e-b0df-a3da1fc58032
ms.date: 12/05/2018
ms.keywords: Application property [RDP], Application property [RDP],IRDPSRAPIWindow interface, Application property [RDP],RDPSRAPIWindow object, IRDPSRAPIWindow interface [RDP],Application property, IRDPSRAPIWindow.Application, IRDPSRAPIWindow.get_Application, IRDPSRAPIWindow::Application, IRDPSRAPIWindow::get_Application, RDPSRAPIWindow object [RDP],Application property, get_Application, rdp.irdpsrapiwindow_application, rdpencomapi/IRDPSRAPIWindow::Application, rdpencomapi/IRDPSRAPIWindow::get_Application
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
 - IRDPSRAPIWindow::get_Application
 - rdpencomapi/IRDPSRAPIWindow::get_Application
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
 - IRDPSRAPIWindow.Application
 - IRDPSRAPIWindow.get_Application
 - RDPSRAPIWindow.Application
---

# IRDPSRAPIWindow::get_Application


## -description

Returns a pointer to the application object that the window belongs to. All the window objects are parented to applications. This method provides easy access to the parent of the window.

This property is read-only.

## -parameters

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiwindow">IRDPSRAPIWindow</a>