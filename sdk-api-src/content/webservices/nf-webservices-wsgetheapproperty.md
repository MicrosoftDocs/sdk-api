---
UID: NF:webservices.WsGetHeapProperty
title: WsGetHeapProperty function
author: windows-sdk-content
description: Retrieves a particular property of a specified Heap.
old-location: wsw\wsgetheapproperty.htm
tech.root: wsw
ms.assetid: c463924a-1491-4d65-86ed-827327e560b9
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsGetHeapProperty, WsGetHeapProperty function [Web Services for Windows], webservices/WsGetHeapProperty, wsw.wsgetheapproperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WsGetHeapProperty
: 
---

# WsGetHeapProperty function


## -description


Retrieves a particular property of a specified Heap.
            


## -parameters




### -param heap [in]

A pointer to the <b>Heap</b> object to that contains the desired property data.  


### -param id [in]

This is a <a href="https://msdn.microsoft.com/e55122e4-fc18-4e1a-b34e-c661b555a062">WS_HEAP_PROPERTY_ID</a> enumerator that identifies the desired property.
                


### -param value

A reference to the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

The buffer size allocated by the caller for the retrieved property value.
                


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



