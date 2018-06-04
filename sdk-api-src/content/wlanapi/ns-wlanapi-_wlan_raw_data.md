---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _WLAN_RAW_DATA structure


## -description


The <b>WLAN_RAW_DATA</b> structure contains raw data in the form of a blob that is used by some Native Wifi functions.


## -struct-fields




### -field dwDataSize

The size, in bytes, of the <b>DataBlob</b> member. The maximum value of the <b>dwDataSize</b> may be restricted by type of data that is stored in the <b>WLAN_RAW_DATA</b> structure.


### -field DataBlob.unique

 


### -field DataBlob.size_is

 


### -field DataBlob.size_is.dwDataSize

 


### -field DataBlob

The data blob.


## -remarks



The <b>WLAN_RAW_DATA</b> structure is a raw data structure used to hold a data entry used by some Native Wifi functions. The data structure is in the form of a generalized blob that can contain any type of data.

The <a href="https://msdn.microsoft.com/cf30b285-9694-4ab0-ad13-c1ec4d8cb6e1">WlanScan</a> function uses the  <b>WLAN_RAW_DATA</b> structure. The  <i>pIeData</i> parameter passed to the <b>WlanScan</b> function points to a  <b>WLAN_RAW_DATA</b> structure currently used to contain an information element to include in probe requests. This <b>WLAN_RAW_DATA</b> structure passed to the <b>WlanScan</b> function can contain a proximity service discovery (PSD) information element (IE) data entry.   

When the <b>WLAN_RAW_DATA</b> structure is used to store a PSD IE, the <b>DOT11_PSD_IE_MAX_DATA_SIZE</b> constant defined in the <i>Wlanapi.h</i> header file is the maximum value of the <b>dwDataSize</b> member.<table>
<tr>
<th>Constant</th>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td><b>DOT11_PSD_IE_MAX_DATA_SIZE</b></td>
<td>240</td>
<td>The maximum data size, in bytes, of a PSD IE data entry.</td>
</tr>
</table>
 



For more information about PSD IEs, including a discussion of the format of an IE, see the  <a href="https://msdn.microsoft.com/eea402d3-9a5f-4446-bf6c-9ab8430f9c60">WlanSetPsdIEDataList</a> function.




## -see-also




<a href="https://msdn.microsoft.com/e0e59abf-1a78-4c7f-b044-2d4c75328329">WLAN_RAW_DATA_LIST</a>



<a href="https://msdn.microsoft.com/cf30b285-9694-4ab0-ad13-c1ec4d8cb6e1">WlanScan</a>



<a href="https://msdn.microsoft.com/eea402d3-9a5f-4446-bf6c-9ab8430f9c60">WlanSetPsdIEDataList</a>
 

 

