---
UID: NF:shdeprecated.IExpDispSupport.FindConnectionPoint
title: IExpDispSupport::FindConnectionPoint (shdeprecated.h)
description: Deprecated. Gets connection points for browser events.
helpviewer_keywords: ["DIID_DWebBrowserEvents","DIID_DWebBrowserEvents2","FindConnectionPoint","FindConnectionPoint method [Windows Shell]","FindConnectionPoint method [Windows Shell]","IExpDispSupport interface","IExpDispSupport interface [Windows Shell]","FindConnectionPoint method","IExpDispSupport.FindConnectionPoint","IExpDispSupport::FindConnectionPoint","IID_IPropertyNotifySink","shdeprecated/IExpDispSupport::FindConnectionPoint","shell.IExpDispSupport_FindCIE4ConnectionPoint","zone_IExpDispSupport_FindCIE4ConnectionPoint"]
old-location: shell\IExpDispSupport_FindCIE4ConnectionPoint.htm
tech.root: shell
ms.assetid: ef8d4e8c-7f85-4920-b149-1bf277d3fd5e
ms.date: 08/02/2022
ms.keywords: DIID_DWebBrowserEvents, DIID_DWebBrowserEvents2, FindConnectionPoint, FindConnectionPoint method [Windows Shell], FindConnectionPoint method [Windows Shell],IExpDispSupport interface, IExpDispSupport interface [Windows Shell],FindConnectionPoint method, IExpDispSupport.FindConnectionPoint, IExpDispSupport::FindConnectionPoint, IID_IPropertyNotifySink, shdeprecated/IExpDispSupport::FindConnectionPoint, shell.IExpDispSupport_FindCIE4ConnectionPoint, zone_IExpDispSupport_FindCIE4ConnectionPoint
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
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
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IExpDispSupport::FindConnectionPoint
 - shdeprecated/IExpDispSupport::FindConnectionPoint
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IExpDispSupport.FindConnectionPoint
---

# IExpDispSupport::FindConnectionPoint


## -description

Deprecated. Gets connection points for browser events.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

The IID of the interface on the connection point container whose connection point object is being requested. One of the following values.



#### DIID_DWebBrowserEvents

Value that indicates a member of the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768309(v=vs.85)">DWebBrowserEvents</a> interface.



#### DIID_DWebBrowserEvents2

Value that indicates a member of the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768283(v=vs.85)">DWebBrowserEvents2</a> interface.



#### IID_IPropertyNotifySink

Value that indicates a member of the <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink">IPropertyNotifySink</a> interface.

### -param ppccp [out]

Type: <b>CIE4ConnectionPoint**</b>

The address of a pointer to the browser connection point.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IExpDispSupport::FindCIE4ConnectionPoint</b> was created specifically for use with Windows Internet Explorer 4.0.