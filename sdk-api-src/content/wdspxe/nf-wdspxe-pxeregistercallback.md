---
UID: NF:wdspxe.PxeRegisterCallback
title: PxeRegisterCallback function (wdspxe.h)
description: Registers callback functions for different notification events.
helpviewer_keywords: ["PXE_CALLBACK_MAX","PXE_CALLBACK_RECV_REQUEST","PXE_CALLBACK_SERVICE_CONTROL","PXE_CALLBACK_SHUTDOWN","PxeRegisterCallback","PxeRegisterCallback function [Windows Deployment Services]","wds.pxeregistercallback","wdspxe/PxeRegisterCallback"]
old-location: wds\pxeregistercallback.htm
tech.root: wds
ms.assetid: e4d7295a-99ef-4dcb-8e40-b5a5383356b5
ms.date: 12/05/2018
ms.keywords: PXE_CALLBACK_MAX, PXE_CALLBACK_RECV_REQUEST, PXE_CALLBACK_SERVICE_CONTROL, PXE_CALLBACK_SHUTDOWN, PxeRegisterCallback, PxeRegisterCallback function [Windows Deployment Services], wds.pxeregistercallback, wdspxe/PxeRegisterCallback
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PxeRegisterCallback
 - wdspxe/PxeRegisterCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeRegisterCallback
---

# PxeRegisterCallback function


## -description

Registers callback functions for different notification events.

## -parameters

### -param hProvider [in]

<b>HANDLE</b> passed to the 
      <a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function.

### -param CallbackType [in]

Specifies the callback that is being registered.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_RECV_REQUEST"></a><a id="pxe_callback_recv_request"></a><dl>
<dt><b>PXE_CALLBACK_RECV_REQUEST</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Register the <a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a> 
        callback. This callback must be registered while the provider is processing the 
        <a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function or the 
        provider will be shut down.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_SHUTDOWN"></a><a id="pxe_callback_shutdown"></a><dl>
<dt><b>PXE_CALLBACK_SHUTDOWN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Register the <a href="/windows/desktop/Wds/pxeprovidershutdown">PxeProviderShutdown</a> 
        callback. This callback must be registered while the provider is processing the 
        <a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a> function or the 
        provider will be shut down.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_SERVICE_CONTROL"></a><a id="pxe_callback_service_control"></a><dl>
<dt><b>PXE_CALLBACK_SERVICE_CONTROL</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Register the 
        <a href="/windows/desktop/Wds/pxeproviderservicecontrol">PxeProviderServiceControl</a> callback.

</td>
</tr>
<tr>
<td width="40%"><a id="PXE_CALLBACK_MAX"></a><a id="pxe_callback_max"></a><dl>
<dt><b>PXE_CALLBACK_MAX</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Used to determine an out-of-range index. Values greater than or equal to 
        <b>PXE_CALLBACK_MAX</b> are not valid.

</td>
</tr>
</table>

### -param pCallbackFunction [in]

Address of the callback function. The function signature varies depending on the 
      <i>CallbackType</i> parameter.

### -param pContext [in]

Context value to be passed to the callback function.

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

## -see-also

<a href="/windows/desktop/Wds/pxeproviderinitialize">PxeProviderInitialize</a>



<a href="/windows/desktop/Wds/pxeproviderrecvrequest">PxeProviderRecvRequest</a>



<a href="/windows/desktop/Wds/pxeproviderservicecontrol">PxeProviderServiceControl</a>



<a href="/windows/desktop/Wds/pxeprovidershutdown">PxeProviderShutdown</a>



<a href="/windows/desktop/Wds/windows-deployment-services-server-functions">Windows Deployment Services Server Functions</a>