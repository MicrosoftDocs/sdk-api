---
UID: NF:mfidl.IMFContentProtectionManager.BeginEnableContent
title: IMFContentProtectionManager::BeginEnableContent (mfidl.h)
author: windows-sdk-content
description: Begins an asynchronous request to perform a content enabling action.
old-location: mf\imfcontentprotectionmanager_beginenablecontent.htm
tech.root: medfound
ms.assetid: 2f422135-8e5f-41fb-a709-77636d1b451b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: 2f422135-8e5f-41fb-a709-77636d1b451b, BeginEnableContent, BeginEnableContent method [Media Foundation], BeginEnableContent method [Media Foundation],IMFContentProtectionManager interface, IMFContentProtectionManager interface [Media Foundation],BeginEnableContent method, IMFContentProtectionManager.BeginEnableContent, IMFContentProtectionManager::BeginEnableContent, mf.imfcontentprotectionmanager_beginenablecontent, mfidl/IMFContentProtectionManager::BeginEnableContent
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFContentProtectionManager::BeginEnableContent


## -description


Begins an asynchronous request to perform a content enabling action.

This method requests the application to perform a specific step needed to acquire rights to the content, using a content enabler object.


## -parameters




### -param pEnablerActivate [in]

Pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of a content enabler object. To create the content enabler, call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> and request the <a href="https://msdn.microsoft.com/45d02bd0-1104-47ec-8559-8cc51590fc62">IMFContentEnabler</a> interface. The application should use the methods in <b>IMFContentEnabler</b> to complete the content enabling action.
          


### -param pTopo [in]

Pointer to the <a href="https://msdn.microsoft.com/f293e9ee-9bd2-4b3e-a4ff-53457ee910f6">IMFTopology</a> interface of the pending topology.
          


### -param pCallback [in]

Pointer to the <a href="https://msdn.microsoft.com/7edff985-da59-4cc0-96de-1a92e03a7d41">IMFAsyncCallback</a> interface of a callback object. When the operation is complete, the application should call <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">IMFAsyncCallback::Invoke</a> on the callback.
          


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.
              

</td>
</tr>
</table>
 




## -remarks



Do not block within this callback method. Instead, perform the content enabling action asynchronously on another thread. When the operation is finished, notify the protected media path (PMP) through the <i>pCallback</i> parameter.

If you return a success code from this method, you must call <a href="https://msdn.microsoft.com/22473605-637e-4783-a8cb-98248b0a0327">Invoke</a> on the callback. Conversely, if you return an error code from this method, you must not call <b>Invoke</b>. If the operation fails after the method returns a success code, use status code on the <a href="https://msdn.microsoft.com/8c95b1de-8974-445c-8070-41552ea83e53">IMFAsyncResult</a> object to report the error.

After the callback is invoked, the PMP will call the application's <a href="https://msdn.microsoft.com/10893a0c-5476-4b7d-aad7-845a4ba70335">IMFContentProtectionManager::EndEnableContent</a> method to complete the asynchronous call.

This method is not necessarily called every time the application plays protected content. Generally, the method will not be called if the user has a valid, up-to-date license for the content. Internally, the input trust authority (ITA) determines whether <b>BeginEnableContent</b> is called, based on the content provider's DRM policy. For more information, see <a href="https://msdn.microsoft.com/e88806ae-0041-4b4a-a8df-69718a651e82">Protected Media Path</a>.




## -see-also




<a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a>



<a href="https://msdn.microsoft.com/0dba0384-eac7-456a-af9f-86eb944cdb2e">IMFContentProtectionManager</a>
 

 

