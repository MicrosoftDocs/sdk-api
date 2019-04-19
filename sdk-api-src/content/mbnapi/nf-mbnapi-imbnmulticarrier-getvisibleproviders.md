---
UID: NF:mbnapi.IMbnMultiCarrier.GetVisibleProviders
title: IMbnMultiCarrier::GetVisibleProviders (mbnapi.h)
author: windows-sdk-content
description: Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers.
old-location: mbn\imbnmulticarrier_getvisibleproviders.htm
tech.root: mbn
ms.assetid: AC11D275-C6E3-48EE-B3DA-C9BC8648D49D
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetVisibleProviders, GetVisibleProviders method [Microsoft Broadband Networks], GetVisibleProviders method [Microsoft Broadband Networks],IMbnMultiCarrier interface, IMbnMultiCarrier interface [Microsoft Broadband Networks],GetVisibleProviders method, IMbnMultiCarrier.GetVisibleProviders, IMbnMultiCarrier::GetVisibleProviders, mbn.imbnmulticarrier_getvisibleproviders, mbnapi/IMbnMultiCarrier::GetVisibleProviders
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mbnapi.h
api_name:
 - IMbnMultiCarrier.GetVisibleProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnMultiCarrier::GetVisibleProviders


## -description


Gets the list of visible providers in the current area for a multi-carrier device minus preferred and registered providers.


## -parameters




### -param age [out]

A pointer to the time, in seconds, since the last refresh of the visible provider list for the device.


### -param visibleProviders [out, retval]

Pointer to an array of <a href="https://msdn.microsoft.com/9D681192-1E40-4314-8E7F-8934AA8162D3">MBN_PROVIDER2</a> structures that contains the list of providers for the interface. If this method returns any value other than <b>S_OK</b>, <i>visibleProviders</i> is <b>NULL</b>. When <b>GetVisibleProviders</b> returns <b>S_OK</b>, the calling application must free the allocated memory by calling <a href="https://msdn.microsoft.com/fc94f7e7-b903-4c78-905c-54df1f8d13fa">SafeArrayDestroy</a>. 




## -returns



This method can return one of these values.

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
The method completed successfully. <i>visibleProviders</i> contains valid values. Based on the age of the information, the calling application can decide to issue a new call to <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available. An active network scan is in progress. The calling application can get notified when the device capabilities are available by registering for the <a href="https://msdn.microsoft.com/EF1A39DB-351F-4105-BE56-C59477A67EC6">OnScanNetworkComplete</a> method of <a href="https://msdn.microsoft.com/F7CAF21B-F487-4F35-806B-312B5246C1B2">IMbnMultiCarrierEvents</a>


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_INVALID_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Mobile Broadband's cache of the visible network list is invalid. The calling application should call <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a> to populate the cache.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_SUPPORTED)</b></dt>
</dl>
</td>
<td width="60%">
The operation is not supported by the device. This may be returned by devices which do not support multi-carrier.

</td>
</tr>
</table>
 




## -remarks



This method returns the list of currently visible providers. CDMA devices will report only their home provider if any network in their preferred roaming list (PRL) is available.

To avoid frequent network scan operations,  Windows maintains a list of recent scan operations and the provider list is returned from the cached list.

An application can call this method to get a list of visible providers upon the completion of <a href="https://msdn.microsoft.com/D249B5D4-B2C3-436A-B38A-041289422F12">ScanNetwork</a>.

This list contains all the currently visible networks available at the user’s location excluding the ones reported by current registered provider and the list of preferred providers.  This list contains network entries that users have not subscribed to.  This list providers the user with an additional set of network choices they can potentially sign up for.




## -see-also




<a href="https://msdn.microsoft.com/E40517CE-3169-4F20-A572-EDBC8FEC2862">IMbnMultiCarrier</a>
 

 

