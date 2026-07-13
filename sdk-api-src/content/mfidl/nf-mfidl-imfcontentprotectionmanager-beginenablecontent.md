---
UID: NF:mfidl.IMFContentProtectionManager.BeginEnableContent
title: IMFContentProtectionManager::BeginEnableContent (mfidl.h)
description: Begins an asynchronous request to perform a content enabling action.
helpviewer_keywords: ["2f422135-8e5f-41fb-a709-77636d1b451b","BeginEnableContent","BeginEnableContent method [Media Foundation]","BeginEnableContent method [Media Foundation]","IMFContentProtectionManager interface","IMFContentProtectionManager interface [Media Foundation]","BeginEnableContent method","IMFContentProtectionManager.BeginEnableContent","IMFContentProtectionManager::BeginEnableContent","mf.imfcontentprotectionmanager_beginenablecontent","mfidl/IMFContentProtectionManager::BeginEnableContent"]
old-location: mf\imfcontentprotectionmanager_beginenablecontent.htm
tech.root: mf
ms.assetid: 2f422135-8e5f-41fb-a709-77636d1b451b
ms.date: 12/05/2018
ms.keywords: 2f422135-8e5f-41fb-a709-77636d1b451b, BeginEnableContent, BeginEnableContent method [Media Foundation], BeginEnableContent method [Media Foundation],IMFContentProtectionManager interface, IMFContentProtectionManager interface [Media Foundation],BeginEnableContent method, IMFContentProtectionManager.BeginEnableContent, IMFContentProtectionManager::BeginEnableContent, mf.imfcontentprotectionmanager_beginenablecontent, mfidl/IMFContentProtectionManager::BeginEnableContent
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFContentProtectionManager::BeginEnableContent
 - mfidl/IMFContentProtectionManager::BeginEnableContent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFContentProtectionManager.BeginEnableContent
---

# IMFContentProtectionManager::BeginEnableContent


## -description

Begins an asynchronous request to perform a content enabling action.

This method requests the application to perform a specific step needed to acquire rights to the content, using a content enabler object.

## -parameters

### -param pEnablerActivate [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> interface of a content enabler object. To create the content enabler, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject">IMFActivate::ActivateObject</a> and request the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a> interface. The application should use the methods in <b>IMFContentEnabler</b> to complete the content enabling action.

### -param pTopo [in]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the pending topology.

### -param pCallback [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback">IMFAsyncCallback</a> interface of a callback object. When the operation is complete, the application should call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> on the callback.

### -param punkState [in]

Reserved. Currently this parameter is always <b>NULL</b>.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
</table>

## -remarks

Do not block within this callback method. Instead, perform the content enabling action asynchronously on another thread. When the operation is finished, notify the protected media path (PMP) through the <i>pCallback</i> parameter.

If you return a success code from this method, you must call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">Invoke</a> on the callback. Conversely, if you return an error code from this method, you must not call <b>Invoke</b>. If the operation fails after the method returns a success code, use status code on the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> object to report the error.

After the callback is invoked, the PMP will call the application's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent">IMFContentProtectionManager::EndEnableContent</a> method to complete the asynchronous call.

This method is not necessarily called every time the application plays protected content. Generally, the method will not be called if the user has a valid, up-to-date license for the content. Internally, the input trust authority (ITA) determines whether <b>BeginEnableContent</b> is called, based on the content provider's DRM policy. For more information, see <a href="/windows/desktop/medfound/protected-media-path">Protected Media Path</a>.

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager">IMFContentProtectionManager</a>