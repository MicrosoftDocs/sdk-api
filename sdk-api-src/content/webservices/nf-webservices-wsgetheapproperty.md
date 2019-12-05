---
UID: NF:webservices.WsGetHeapProperty
title: WsGetHeapProperty function (webservices.h)
description: Retrieves a particular property of a specified Heap.
old-location: wsw\wsgetheapproperty.htm
tech.root: wsw
ms.assetid: c463924a-1491-4d65-86ed-827327e560b9
ms.date: 12/05/2018
ms.keywords: WsGetHeapProperty, WsGetHeapProperty function [Web Services for Windows], webservices/WsGetHeapProperty, wsw.wsgetheapproperty
ms.topic: function
f1_keywords:
- webservices/WsGetHeapProperty
dev_langs:
- c++
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- WebServices.dll
api_name:
- WsGetHeapProperty
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsGetHeapProperty function


## -description


Retrieves a particular property of a specified Heap.
            


## -parameters




### -param heap [in]

A pointer to the <b>Heap</b> object to that contains the desired property data.  


### -param id [in]

This is a <a href="https://docs.microsoft.com/windows/desktop/api/webservices/ns-webservices-ws_heap_property">WS_HEAP_PROPERTY_ID</a> enumerator that identifies the desired property.
                


### -param value

A reference to the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The buffer size allocated by the caller for the retrieved property value.
                


### -param error [in, optional]

A  pointer to a <a href="https://docs.microsoft.com/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



