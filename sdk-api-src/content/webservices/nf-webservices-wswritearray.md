---
UID: NF:webservices.WsWriteArray
title: WsWriteArray function (webservices.h)
description: This operation sends a series of elements to an XML Writer.
helpviewer_keywords: ["WsWriteArray","WsWriteArray function [Web Services for Windows]","webservices/WsWriteArray","wsw.wswritearray"]
old-location: wsw\wswritearray.htm
tech.root: wsw
ms.assetid: c172dc3c-0c0a-4c92-8103-465b636d0c61
ms.date: 12/05/2018
ms.keywords: WsWriteArray, WsWriteArray function [Web Services for Windows], webservices/WsWriteArray, wsw.wswritearray
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsWriteArray
 - webservices/WsWriteArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsWriteArray
---

# WsWriteArray function


## -description

This operation sends a series of elements to an XML Writer.

## -parameters

### -param writer [in]

A pointer to the Writer where the elements are written.

### -param localName [in]

A pointer to the localName of the repeating element.

### -param ns [in]

A pointer to the namespace of the repeating element.

### -param valueType [in]

The value type for the elements

### -param array

A void pointer to the values written to <i>writer</i>.  The size of the items is determined by  value type.
          <div class="alert"><b>Note</b>  See <a href="/windows/desktop/api/webservices/ne-webservices-ws_value_type">WS_VALUE_TYPE</a> for more information.
        </div>
<div> </div>

### -param arraySize [in]

The total byte length of the array.

### -param itemOffset [in]

The item offset within the array to write.

### -param itemCount [in]

The total number of items to write from the array.

### -param error [in, optional]

A  pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> object where additional information about the error should be stored if the function fails.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is semantically equivalent to using <a href="/windows/desktop/api/webservices/nf-webservices-wswritestartelement">WsWriteStartElement</a>,
        <a href="/windows/desktop/api/webservices/nf-webservices-wswritevalue">WsWriteValue</a> and <a href="/windows/desktop/api/webservices/nf-webservices-wswriteendelement">WsWriteEndElement</a> in a loop, but is more efficient.