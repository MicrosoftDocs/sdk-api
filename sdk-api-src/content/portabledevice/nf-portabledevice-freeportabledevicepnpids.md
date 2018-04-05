---
UID: NF:portabledevice.FreePortableDevicePnPIDs
title: FreePortableDevicePnPIDs function
author: windows-driver-content
description: Frees the Plug and Play (PnP) identifiers that are retrieved by the IPortableDeviceManager::GetDevices or IPortableDeviceServiceManager::GetDeviceServices methods.
old-location: wpdsdk\freeportabledevicepnpids.htm
old-project: wpd_sdk
ms.assetid: b86f7733-81a3-4b60-bb7c-840c75f8d03f
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: FreePortableDevicePnPIDs, FreePortableDevicePnPIDs function [Windows Portable Devices SDK], portabledevice/FreePortableDevicePnPIDs, wpdsdk.freeportabledevicepnpids
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: portabledevice.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	PortableDevice.h
api_name:
-	FreePortableDevicePnPIDs
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# FreePortableDevicePnPIDs function


## -description


The <b>FreePortableDevicePnPIDs</b> helper function  frees the Plug and Play (PnP) identifiers that are retrieved by the <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">IPortableDeviceManager::GetDevices</a> or <a href="https://msdn.microsoft.com/d6b06f4d-c07e-4cd4-b96e-e8b9b4f98df8">IPortableDeviceServiceManager::GetDeviceServices</a> methods.


## -parameters




### -param pPnPIDs

The array of Plug and Play (PnP) identifiers to be freed.
          


### -param cPnPIDs

The number of identifiers in the array specified by the <i>pPnPIDs</i> parameter.
          


## -returns



This function does not return a value.




## -remarks



The application is responsible for freeing the array of pointers that it allocates.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
// Allocate an array of LPWSTR pointers.
	LPWSTR* pPnpDeviceIDs = new LPWSTR[cPnpDeviceIDs];
if (pPnpDeviceIDs != NULL)
{
	hr = pPortableDeviceManager-&gt;;GetDevices(pPnpDeviceIDs, &amp;cPnpDeviceIDs);
	if (SUCCEEDED(hr))
	{
	    // Free all returned PnPDeviceID strings allocated by IPortableDeviceManager::GetDevices.
     FreePortableDevicePnPIDs(pPnpDeviceIDs, cPnpDeviceIDs);
     // Application is responsible for deleting the array of LPWSTR pointers.
     delete [] pPnpDeviceIDs;
     pPnpDeviceIDs = NULL;		
 }
} </pre>
</td>
</tr>
</table></span></div>


