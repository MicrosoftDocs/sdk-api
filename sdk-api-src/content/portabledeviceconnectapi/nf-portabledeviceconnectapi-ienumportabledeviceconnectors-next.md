---
UID: NF:portabledeviceconnectapi.IEnumPortableDeviceConnectors.Next
title: IEnumPortableDeviceConnectors::Next
author: windows-driver-content
description: Retrieves the next one or more IPortableDeviceConnector objects in the enumeration sequence.
old-location: wpdsdk\ienumportabledeviceconnectors_next.htm
old-project: wpd_sdk
ms.assetid: 5aed563a-5ecc-49c0-8a0c-622405453896
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IEnumPortableDeviceConnectors interface [Windows Portable Devices SDK],Next method, IEnumPortableDeviceConnectors.Next, IEnumPortableDeviceConnectors::Next, Next, Next method [Windows Portable Devices SDK], Next method [Windows Portable Devices SDK],IEnumPortableDeviceConnectors interface, devpkey/IEnumPortableDeviceConnectors::Next, portabledeviceconnectapi/IEnumPortableDeviceConnectors::Next, wpdsdk.ienumportabledeviceconnectors_next
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceconnectapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Portabledeviceconnectapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGuids.lib
-	PortableDeviceGuids.dll
api_name:
-	IEnumPortableDeviceConnectors.Next
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IEnumPortableDeviceConnectors::Next


## -description


The <b>Next</b> method retrieves the next one or more <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> objects in the enumeration sequence.


## -parameters




### -param cRequested [in]

The number of requested devices. This value also indicates the number of elements in the caller-allocated array specified by the <i>pConnectors</i> parameter.


### -param pConnectors [out]

An array of <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> pointers, each specifying a paired MTP Bluetooth device. The caller must allocate an array of <b>IPortableDeviceConnector</b> pointers, with the array length specified by the <i>cRequested</i> parameter. On successful return, the caller must free both the array and the returned pointers. The <b>IPortableDeviceConnector</b> interfaces are freed by calling the <b>IUnknown::Release</b> method.


### -param pcFetched [in, out]

The number of <a href="https://msdn.microsoft.com/c6eb1103-2395-431d-9130-1e1f2cc9ae96">IPortableDeviceConnector</a> interfaces that are actually retrieved. If no <b>IPortableDeviceConnector</b> interfaces are retrieved and the return value is <b>S_FALSE</b>, there are no more <b>IPortableDeviceConnector</b> interfaces to enumerate.


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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more MTP Bluetooth devices to enumerate.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/99aa1e89-5e20-4f6e-82b5-acf63305eba0">IEnumPortableDeviceConnectors</a>
 

 

