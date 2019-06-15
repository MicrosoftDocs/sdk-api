---
UID: NF:webservices.WsRegisterOperationForCancel
title: WsRegisterOperationForCancel function (webservices.h)
author: windows-sdk-content
description: A service operation can use this function to register for a cancel notification. It is only valid to call this API when the service operation is executing. The behavior for calling it after the completion of Service Operation is not supported.
old-location: wsw\wsregisteroperationforcancel.htm
tech.root: wsw
ms.assetid: 3e456814-f70f-47ab-b866-f0b73d5cd35e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsRegisterOperationForCancel, WsRegisterOperationForCancel function [Web Services for Windows], webservices/WsRegisterOperationForCancel, wsw.wsregisteroperationforcancel
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WsRegisterOperationForCancel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WsRegisterOperationForCancel function


## -description


A service operation can use this function to register for a cancel notification. 
                It is only valid to call this API when the service operation is executing. The behavior 
                for calling it after the completion of Service Operation is not supported.
            

While this API is being called and the runtime has determined that the cancellation of the 
                service operation is necessary, it can call the callback during the call to this API by the application. 
            

The caller should therefore assume that the runtime may call on the callback 
                <a href="https://docs.microsoft.com/windows/desktop/api/webservices/nc-webservices-ws_operation_cancel_callback">WS_OPERATION_CANCEL_CALLBACK</a> as soon as the WsRegisterOperationForCancel is called.
            


## -parameters




### -param context [in]

The context that the property value is being obtained for.


### -param cancelCallback [in]

Function pointer for cancel notification function.
                


### -param freestateCallback [in, optional]

A optional parameter specifying the function pointer to the free state call. 
                


### -param userState [in, optional]

A optional parameter specifying the application specific state which can be used to identify call data. 
                


### -param error [in, optional]

Specifies where additional error information should be stored if the function fails.
                


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



