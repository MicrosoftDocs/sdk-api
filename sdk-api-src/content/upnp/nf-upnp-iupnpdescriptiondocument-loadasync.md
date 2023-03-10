---
UID: NF:upnp.IUPnPDescriptionDocument.LoadAsync
title: IUPnPDescriptionDocument::LoadAsync (upnp.h)
description: The LoadAsync method loads a document asynchronously. This method returns control to the caller immediately, and uses the specified callback to notify the caller when the operation is complete.
helpviewer_keywords: ["IUPnPDescriptionDocument interface [UPnP APIs]","LoadAsync method","IUPnPDescriptionDocument.LoadAsync","IUPnPDescriptionDocument::LoadAsync","LoadAsync","LoadAsync method [UPnP APIs]","LoadAsync method [UPnP APIs]","IUPnPDescriptionDocument interface","_upnp_iupnpdescriptiondocument_loadasync","upnp.iupnpdescriptiondocument_loadasync","upnp/IUPnPDescriptionDocument::LoadAsync"]
old-location: upnp\iupnpdescriptiondocument_loadasync.htm
tech.root: upnp
ms.assetid: bfb1d833-13e8-4ffe-832d-f6640a42055a
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocument interface [UPnP APIs],LoadAsync method, IUPnPDescriptionDocument.LoadAsync, IUPnPDescriptionDocument::LoadAsync, LoadAsync, LoadAsync method [UPnP APIs], LoadAsync method [UPnP APIs],IUPnPDescriptionDocument interface, _upnp_iupnpdescriptiondocument_loadasync, upnp.iupnpdescriptiondocument_loadasync, upnp/IUPnPDescriptionDocument::LoadAsync
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDescriptionDocument::LoadAsync
 - upnp/IUPnPDescriptionDocument::LoadAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.LoadAsync
---

# IUPnPDescriptionDocument::LoadAsync


## -description

The 
<b>LoadAsync</b> method loads a document asynchronously. This method returns control to the caller immediately, and uses the specified callback to notify the caller when the operation is complete.

## -parameters

### -param bstrUrl [in]

Specifies the URL of the document to load. If the URL specified is a relative URL, the server name is prepended to the value of <i>bstrUrl</i>.

### -param punkCallback [in]

Reference to an <b>IUnknown</b> specifying the callback that the UPnP framework uses to notify the caller when the operation is complete. If the load operation did not fail immediately, this callback indicates whether or not the load operation succeeded or failed. The object referred to by <i>pUnkCallback</i> must support either the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocumentcallback">IUPnPDescriptionDocumentCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h, or one of the following UPnP return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have a device element It is missing either from the root element or the <b>DeviceList</b> element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The XML document is missing one of the required elements from the <b>Device</b> element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ICON_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have an icon element. It is missing from the <b>IconList</b> element, or the <b>DeviceList</b> element does not contain an <b>IconList</b> element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ICON_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The XML document is missing one of the required elements from the <b>Icon</b> element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ROOT_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have a root element at the top level of the document.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_SERVICE_ELEMENT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The XML document does not have a service element. It is missing from the <b>ServiceList</b> element, or the <b>DeviceList</b> element does not contain a <b>ServiceList</b> element.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_SERVICE_NODE_INCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The XML document is missing one of the required elements from the <b>Service</b> element.

</td>
</tr>
</table>

## -remarks

This method should not be called from a user interface thread because it can take a long time for the method to return.

If you invoke this method for the same object immediately after a previous invocation, the first invocation of 
<b>LoadAsync</b> is aborted. To avoid this, wait for the 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocumentcallback-loadcomplete">IUPnPDescriptionDocumentCallback::LoadComplete</a> callback, and then use 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-get_loadresult">LoadResult</a> to view the state information.

If the 
<b>LoadAsync</b> method is called by a script within a Web page, <i>bstrUrl</i> might be a relative URL. The address of the current Web page is used as the base URL.

If this method is called from a Web page, the URL that the caller specifies must refer to the same server from which the Web page was loaded.

The object referred to by <i>pUnkCallback</i> must either support the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocumentcallback">IUPnPDescriptionDocumentCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. The 
<b>LoadAsync</b> method first queries <i>pUnkCallback</i> for the 
<b>IUPnPDescriptionDocumentCallback</b> interface. If this interface is not supported, the 
<b>LoadAsync</b> method then queries <i>pUnkCallback</i> for the <b>IDispatch</b> interface. If the <b>IDispatch</b> interface is not supported, both checks have failed and the 
<b>LoadAsync</b> method returns E_FAIL.

The callback based on <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> for the 
<b>LoadAsync</b> method works as a script function that takes one parameter. This parameter is the result of the load operation. If the parameter is zero, the load succeeded, and the user can retrieve device objects from the document. If the parameter is non-zero, it describes the error. The value is the same as the error code that the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a> method returns.

In Visual Basic Scripting Edition (VBScript) development software, the second argument must be <b>GetRef</b>(<i>funcname</i>), where <i>funcname</i> is the name of the callback subroutine.

If this function returns S_OK, 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocumentcallback-loadcomplete">IUPnPDescriptionDocumentCallback::LoadComplete</a> is invoked by the UPnP framework.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a>