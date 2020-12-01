---
UID: NC:cmnquery.LPCQPAGEPROC
title: LPCQPAGEPROC (cmnquery.h)
description: Called by the query dialog box to notify the query form extension of events that occur in a query page.
helpviewer_keywords: ["CQPageProc","CQPageProc callback","CQPageProc callback function [Active Directory]","LPCQPAGEPROC","LPCQPAGEPROC callback function pointer [Active Directory]","ad.cqpageproc","cmnquery/CQPageProc"]
old-location: ad\cqpageproc.htm
tech.root: ad
ms.assetid: 11d40439-0877-4870-80f8-88026c448a32
ms.date: 12/05/2018
ms.keywords: CQPageProc, CQPageProc callback, CQPageProc callback function [Active Directory], LPCQPAGEPROC, LPCQPAGEPROC callback function pointer [Active Directory], ad.cqpageproc, cmnquery/CQPageProc
req.header: cmnquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - LPCQPAGEPROC
 - cmnquery/LPCQPAGEPROC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Cmnquery.h
api_name:
 - LPCQPAGEPROC
---

# LPCQPAGEPROC callback function


## -description

The <b>CQPageProc</b> callback function is called by the query dialog box to notify the query form extension of events that occur in a query page. A pointer to this function is supplied to the query dialog box in the <i>pPageProc</i> member of the <a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqpage">CQPAGE</a> structure. <b>CQPageProc</b> is a placeholder for the query form extension-defined function name.

## -parameters

### -param pPage

Pointer to a <a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqpage">CQPAGE</a> structure that contains data about a query page.

### -param hwnd

Contains the window handle of the query page.

### -param uMsg

Contains a value that identifies the event that this function is called for. This can be one of the <a href="/windows/desktop/AD/messages-communicated-through-user-interfaces">Common Query Page Messages</a>.

### -param wParam

Contains additional message data. The contents of this parameter depend on the value of the <i>uMsg</i> parameter.

### -param lParam

Contains additional message data. The content of this parameter depends on the value of the <i>uMsg</i> parameter.

## -returns

The return value is the result of the message  and depends on the value of the <i>uMsg</i> parameter.

## -see-also

<a href="/windows/desktop/api/cmnquery/nc-cmnquery-lpcqaddpagesproc">CQAddPagesProc</a>



<a href="/windows/desktop/api/cmnquery/ns-cmnquery-cqpage">CQPAGE</a>



<a href="/windows/desktop/AD/messages-communicated-through-user-interfaces">Common Query Page Messages</a>



<a href="/windows/desktop/api/cmnquery/nf-cmnquery-iqueryform-addpages">IQueryForm::AddPages</a>