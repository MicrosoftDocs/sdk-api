---
UID: NF:mfidl.IMFContentProtectionManager.EndEnableContent
title: IMFContentProtectionManager::EndEnableContent (mfidl.h)
description: Ends an asynchronous request to perform a content enabling action. This method is called by the protected media path (PMP) to complete an asynchronous call to IMFContentProtectionManager::BeginEnableContent.
helpviewer_keywords: ["10893a0c-5476-4b7d-aad7-845a4ba70335","EndEnableContent","EndEnableContent method [Media Foundation]","EndEnableContent method [Media Foundation]","IMFContentProtectionManager interface","IMFContentProtectionManager interface [Media Foundation]","EndEnableContent method","IMFContentProtectionManager.EndEnableContent","IMFContentProtectionManager::EndEnableContent","mf.imfcontentprotectionmanager_endenablecontent","mfidl/IMFContentProtectionManager::EndEnableContent"]
old-location: mf\imfcontentprotectionmanager_endenablecontent.htm
tech.root: mf
ms.assetid: 10893a0c-5476-4b7d-aad7-845a4ba70335
ms.date: 12/05/2018
ms.keywords: 10893a0c-5476-4b7d-aad7-845a4ba70335, EndEnableContent, EndEnableContent method [Media Foundation], EndEnableContent method [Media Foundation],IMFContentProtectionManager interface, IMFContentProtectionManager interface [Media Foundation],EndEnableContent method, IMFContentProtectionManager.EndEnableContent, IMFContentProtectionManager::EndEnableContent, mf.imfcontentprotectionmanager_endenablecontent, mfidl/IMFContentProtectionManager::EndEnableContent
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
 - IMFContentProtectionManager::EndEnableContent
 - mfidl/IMFContentProtectionManager::EndEnableContent
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
 - IMFContentProtectionManager.EndEnableContent
---

# IMFContentProtectionManager::EndEnableContent


## -description

Ends an asynchronous request to perform a content enabling action. This method is called by the protected media path (PMP) to complete an asynchronous call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent">IMFContentProtectionManager::BeginEnableContent</a>.

## -parameters

### -param pResult [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult">IMFAsyncResult</a> interface. This pointer is the same value that the application passed to the caller's <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke">IMFAsyncCallback::Invoke</a> method.

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

When the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent">BeginEnableContent</a> method completes asynchronously, the application notifies the PMP by invoking the asynchronous callback. The PMP calls <b>EndEnableContent</b> on the application to get the result code. This method is called on the application's thread from inside the callback method. Therefore, it must not block the thread that invoked the callback.

The application must return the success or failure code of the asynchronous processing that followed the call to <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent">BeginEnableContent</a>.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager">IMFContentProtectionManager</a>