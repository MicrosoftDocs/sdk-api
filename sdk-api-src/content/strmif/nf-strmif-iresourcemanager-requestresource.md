---
UID: NF:strmif.IResourceManager.RequestResource
title: IResourceManager::RequestResource (strmif.h)
author: windows-sdk-content
description: The RequestResource method requests the use of a given registered resource.
old-location: dshow\iresourcemanager_requestresource.htm
tech.root: DirectShow
ms.assetid: b52dc38a-9246-4cef-ba1a-cf1927223183
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IResourceManager interface [DirectShow],RequestResource method, IResourceManager.RequestResource, IResourceManager::RequestResource, IResourceManagerRequestResource, RequestResource, RequestResource method [DirectShow], RequestResource method [DirectShow],IResourceManager interface, dshow.iresourcemanager_requestresource, strmif/IResourceManager::RequestResource
ms.topic: method
f1_keywords: 
 - "strmif/IResourceManager.RequestResource"
dev_langs:
 - c++
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IResourceManager.RequestResource
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IResourceManager::RequestResource


## -description



The <code>RequestResource</code> method requests the use of a given registered resource.




## -parameters




### -param idResource [in]

Resource token retrieved when the resource was registered.


### -param pFocusObject [in]

Pointer to the <b>IUnknown</b> interface of a focus object associated with a request (typically the <b>IUnknown</b> interface of the filter).


### -param pConsumer [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iresourceconsumer">IResourceConsumer</a> interface on the object requesting the resource.


## -returns



Returns an <b>HRESULT</b> value. Returns S_OK if the requested resource is returned, or S_FALSE if the resource is not available, in which case the resource manager will call the requesting object back when the resource becomes available. Any other return is an error.




## -remarks



When there is more than one request for the resource, the resource manager will decide the priority by using the object of focus passed with each request and comparing it to the object of focus passed in the most recent <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">IResourceManager::SetFocus</a> method.

Requests will be filled in the following order of priority:

<ol>
<li>Requests made with exactly the same object of focus as the last <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-setfocus">SetFocus</a> method.</li>
<li>Requests whose object of focus shares a common source filter whose object of focus shares a common filter graph.</li>
<li>Requests in the same process as the focus.</li>
</ol>
While checking this priority, the resource manager will use <b>QueryInterface</b> on the focus object for IID_IFilter. If found, the resource manager will use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> methods to check the filter graph and look for common source filters with the current focus object.

A filter should pass the <b>IUnknown</b> interface of the filter in the <i>pFocusObject</i> parameter. The filter graph manager matches filters to the filter graph and will attempt to trace filters to common source filters when checking objects of focus.

The focus object must be valid for the entire lifetime of the request—until either the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-cancelrequest">IResourceManager::CancelRequest</a> method is called, or the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iresourcemanager-notifyrelease">IResourceManager::NotifyRelease</a> method is called with the <i>bStillWant</i> parameter set to <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iresourcemanager">IResourceManager Interface</a>
 

 

