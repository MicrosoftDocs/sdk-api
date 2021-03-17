---
UID: NF:upnp.IUPnPDeviceFinder.CreateAsyncFind
title: IUPnPDeviceFinder::CreateAsyncFind (upnp.h)
description: The CreateAsyncFind method creates an asynchronous search operation.
helpviewer_keywords: ["CreateAsyncFind","CreateAsyncFind method [UPnP APIs]","CreateAsyncFind method [UPnP APIs]","IUPnPDeviceFinder interface","IUPnPDeviceFinder interface [UPnP APIs]","CreateAsyncFind method","IUPnPDeviceFinder.CreateAsyncFind","IUPnPDeviceFinder::CreateAsyncFind","_upnp_iupnpdevicefinder_createasyncfind","upnp.iupnpdevicefinder_createasyncfind","upnp/IUPnPDeviceFinder::CreateAsyncFind"]
old-location: upnp\iupnpdevicefinder_createasyncfind.htm
tech.root: upnp
ms.assetid: 4461b53f-b630-4b4a-bc68-0cc48ef70594
ms.date: 12/05/2018
ms.keywords: CreateAsyncFind, CreateAsyncFind method [UPnP APIs], CreateAsyncFind method [UPnP APIs],IUPnPDeviceFinder interface, IUPnPDeviceFinder interface [UPnP APIs],CreateAsyncFind method, IUPnPDeviceFinder.CreateAsyncFind, IUPnPDeviceFinder::CreateAsyncFind, _upnp_iupnpdevicefinder_createasyncfind, upnp.iupnpdevicefinder_createasyncfind, upnp/IUPnPDeviceFinder::CreateAsyncFind
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
 - IUPnPDeviceFinder::CreateAsyncFind
 - upnp/IUPnPDeviceFinder::CreateAsyncFind
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
 - IUPnPDeviceFinder.CreateAsyncFind
---

# IUPnPDeviceFinder::CreateAsyncFind


## -description

The 
<b>CreateAsyncFind</b> method creates an asynchronous search operation.

## -parameters

### -param bstrTypeURI [in]

Specifies the uniform resource identifier (URI) for which to search.

### -param dwFlags [in]

Specify zero. This parameter is reserved for future use.

### -param punkDeviceFinderCallback [in]

Reference to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface object that specifies the callback that the UPnP framework must use to communicate the results of this asynchronous search.

The object referred to by <i>pUnkCallback</i> must support either the 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. The object referred to by <i>pUnkCallback</i> might support the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface">IUPnPDeviceFinderAddCallbackWithInterface</a> interface, in addition to the <b>IUPnPDeviceFinderCallback</b> interface.

### -param plFindData [out]

Reference to a <b>LONG</b> that receives the identifier for this particular search. The application must supply this identifier to other asynchronous search methods that are called.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

This method returns immediately; the UPnP framework notifies the caller of any search results using the callback specified by <i>pUnkCallback</i>. This method returns a search identifier; the caller must use the <a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-startasyncfind">IUPnPDeviceFinder::StartAsyncFind</a> to actually begin the search.

In C++, the object referred to by <i>pUnkCallback</i> must support either the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefindercallback">IUPnPDeviceFinderCallback</a> interface or the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. Optionally, the object referred to by <i>pUnkCallback</i>  might support the <a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface">IUPnPDeviceFinderAddCallbackWithInterface</a> interface, in addition to the <b>IUPnPDeviceFinderCallback</b> interface. The UPnP framework first queries <i>pUnkCallback</i> for the <b>IUPnPDeviceFinderAddCallbackWithInterface</b> interface. If the interface is not supported, the UPnP framework next queries <i>pUnkCallback</i> for the <b>IUPnPDeviceFinderCallback</b> interface.  If it is not supported, the UPnP framework then queries <i>pUnkCallback</i> for the <b>IDispatch</b> interface. If the <b>IDispatch</b> interface is not supported, the UPnP framework returns E_FAIL.

In VBScript, the second argument must be <b>GetRef</b>(<i>funcname</i>), where <i>funcname</i> is the name of the callback subroutine.

In Visual Basic, the callback function must be declared with three parameters. The callback function uses the values specified for each parameter: <ul>
<li><i>param1</i> is the Device object of the new device; it is only valid when <i>param3</i> is zero. </li>
<li><i>param2</i> is the UDN of the found or removed device; it is only valid when <i>param3</i> is zero or one. 
</li>
<li><i>param3</i> is the type of callback. Valid values are: <dl>
<dd>0—indicates a new device. 

</dd>
<dd>1—indicates a device has been removed. 

</dd>
<dd>2—indicates the search is complete. 
</dd>
</dl>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevicefinder">IUPnPDeviceFinder</a>



<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdevicefinder-startasyncfind">IUPnPDeviceFinder::StartAsyncFind</a>