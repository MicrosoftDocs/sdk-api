---
UID: NS:wlanapi._WLAN_RAW_DATA
title: "_WLAN_RAW_DATA"
author: windows-sdk-content
description: Contains raw data in the form of a blob that is used by some Native Wifi functions.
old-location: nwifi\dot11_psd_ie_data_entry.htm
old-project: nativewifi
ms.assetid: 5f5ddecb-f841-436c-bf31-c70c95a5d39c
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PWLAN_RAW_DATA, PWLAN_RAW_DATA, PWLAN_RAW_DATA structure pointer [NativeWIFI], WLAN_RAW_DATA, WLAN_RAW_DATA structure [NativeWIFI], _WLAN_RAW_DATA, nwifi.dot11_psd_ie_data_entry, wlanapi/PWLAN_RAW_DATA, wlanapi/WLAN_RAW_DATA"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.redist: 
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
tech.root: 
req.typenames: WLAN_RAW_DATA, *PWLAN_RAW_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_RAW_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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
 

 

