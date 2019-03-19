---
UID: NF:mbnapi.IMbnInterface.GetVisibleProviders
title: IMbnInterface::GetVisibleProviders (mbnapi.h)
author: windows-sdk-content
description: Gets the list of visible providers.
old-location: mbn\imbninterface_getvisibleproviders.htm
tech.root: mbn
ms.assetid: 916c29ee-adb3-402c-b4f3-97b8977f44ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetVisibleProviders, GetVisibleProviders method [Microsoft Broadband Networks], GetVisibleProviders method [Microsoft Broadband Networks],IMbnInterface interface, IMbnInterface interface [Microsoft Broadband Networks],GetVisibleProviders method, IMbnInterface.GetVisibleProviders, IMbnInterface::GetVisibleProviders, mbn.imbninterface_getvisibleproviders, mbnapi/IMbnInterface::GetVisibleProviders
ms.topic: method
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
 - IMbnInterface.GetVisibleProviders
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMbnInterface::GetVisibleProviders


## -description


Gets the list of visible providers.


## -parameters




### -param age [out, retval]

A pointer to the time in seconds since the last refresh of the visible provider list from the device.


### -param visibleProviders [out, retval]

Pointer to an array of  <a href="https://msdn.microsoft.com/f4a02ca2-6be4-4843-a657-5d5dde8be623">MBN_PROVIDER</a> structures that contains the list of providers for the interface.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  Otherwise, upon completion, the calling program must free the allocated memory  by calling <a href="http://go.microsoft.com/fwlink/p/?linkid=121490">SafeArrayDestroy</a>. 


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
The method completed successfully.  <i>visibleProviders</i> contains valid values.  Based on the age of the information, the calling application can decide to issue a new call to <a href="https://msdn.microsoft.com/72db3d85-b7f2-4dae-9637-b003df6e9cf5">ScanNetwork</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  An active network scan is in progress.  The calling application can get notified when the device capabilities are available by registering for the <a href="https://msdn.microsoft.com/6320c76b-b8a6-44dc-88bb-e20a85d5cfca">OnScanNetworkComplete</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_INVALID_CACHE</b></dt>
</dl>
</td>
<td width="60%">
Mobile Broadband's cache of the visible network list is invalid.  The calling application should call <a href="https://msdn.microsoft.com/72db3d85-b7f2-4dae-9637-b003df6e9cf5">ScanNetwork</a> to populate the cache.

</td>
</tr>
</table>
 




## -remarks



This method returns the list of currently visible providers.  CDMA devices will report only their home provider if any network in their preferred roaming list (PRL) is available.

To avoid frequent network scan operations, the operating system maintains a list of recent scan operations and the provider list is returned from the cached list.

An application can call this method to get a list of visible providers upon the completion of <a href="https://msdn.microsoft.com/72db3d85-b7f2-4dae-9637-b003df6e9cf5">ScanNetwork</a>.




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 

