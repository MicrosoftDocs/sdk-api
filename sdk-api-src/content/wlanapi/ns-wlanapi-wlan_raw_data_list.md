---
UID: NS:wlanapi._WLAN_RAW_DATA_LIST
title: WLAN_RAW_DATA_LIST (wlanapi.h)
description: Contains raw data in the form of an array of data blobs that are used by some Native Wifi functions.
helpviewer_keywords: ["*PWLAN_RAW_DATA_LIST","PWLAN_RAW_DATA_LIST","PWLAN_RAW_DATA_LIST structure pointer [NativeWIFI]","WLAN_RAW_DATA_LIST","WLAN_RAW_DATA_LIST structure [NativeWIFI]","nwifi.dot11_psd_ie_data_list","wlanapi/PWLAN_RAW_DATA_LIST","wlanapi/WLAN_RAW_DATA_LIST"]
old-location: nwifi\dot11_psd_ie_data_list.htm
tech.root: nwifi
ms.assetid: e0e59abf-1a78-4c7f-b044-2d4c75328329
ms.date: 12/05/2018
ms.keywords: '*PWLAN_RAW_DATA_LIST, PWLAN_RAW_DATA_LIST, PWLAN_RAW_DATA_LIST structure pointer [NativeWIFI], WLAN_RAW_DATA_LIST, WLAN_RAW_DATA_LIST structure [NativeWIFI], nwifi.dot11_psd_ie_data_list, wlanapi/PWLAN_RAW_DATA_LIST, wlanapi/WLAN_RAW_DATA_LIST'
req.header: wlanapi.h
req.include-header: Wlanapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WLAN_RAW_DATA_LIST, *PWLAN_RAW_DATA_LIST
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLAN_RAW_DATA_LIST
 - wlanapi/_WLAN_RAW_DATA_LIST
 - PWLAN_RAW_DATA_LIST
 - wlanapi/PWLAN_RAW_DATA_LIST
 - WLAN_RAW_DATA_LIST
 - wlanapi/WLAN_RAW_DATA_LIST
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - wlanapi.h
api_name:
 - WLAN_RAW_DATA_LIST
---

# WLAN_RAW_DATA_LIST structure


## -description

The <b>WLAN_RAW_DATA_LIST</b> structure contains raw data in the form of an array of data blobs that are used by some Native Wifi functions.

## -struct-fields

### -field dwTotalSize

The total size, in bytes, of the <b>WLAN_RAW_DATA_LIST</b> structure.

### -field dwNumberOfItems

The number of raw data entries or blobs in the <b>WLAN_RAW_DATA_LIST</b> structure. The maximum value of the <b>dwNumberOfItems</b> may be restricted by the type of data that is stored in the <b>WLAN_RAW_DATA_LIST</b> structure.

### -field dwDataOffset

### -field dwDataSize

### -field DataList

An array of raw data entries or blobs that make up the data list.



#### dwDataOffset

The offset, in bytes, of the data blob from the beginning of current blob descriptor. For details, see the example in the Remarks section below.



#### dwDataSize

The size, in bytes, of the data blob.

## -remarks

The <b>WLAN_RAW_DATA_LIST</b> structure is used to encapsulate a list of data blobs into a flat memory block. It should be interpreted as a list of headers followed by data blobs.

To create 	a <b>WLAN_RAW_DATA_LIST</b>, an application needs to allocate a memory block that is large enough to hold the headers and the data blobs, and then cast the memory block to a pointer to a  <b>WLAN_RAW_DATA_LIST</b> structure.

The following is the memory layout of an example <b>WLAN_RAW_DATA_LIST</b> structure that contains two data blobs.

<table>
<tr>
<td>Memory Offset</td>
<td>Field</td>
<td>Value</td>
<td>Comments</td>
</tr>
<tr>
<td>0</td>
<td>dwTotalSize</td>
<td>84</td>
<td></td>
</tr>
<tr>
<td>4</td>
<td>dwNumberOfItems</td>
<td> 2</td>
<td></td>
</tr>
<tr>
<td>8</td>
<td>dwDataOffset</td>
<td>16</td>
<td>Offset of the first blob: 16 = 24 - 8</td>
</tr>
<tr>
<td>12</td>
<td>dwDataSize</td>
<td>20</td>
<td>Size of the first blob.</td>
</tr>
<tr>
<td>16</td>
<td>dwDataOffset</td>
<td>28</td>
<td>Offset of the second blob: 44 - 16. </td>
</tr>
<tr>
<td>20</td>
<td>dwDataSize</td>
<td>24</td>
<td>Size of the second blob.</td>
</tr>
<tr>
<td>24</td>
<td></td>
<td>20</td>
<td>Start of the first blob. </td>
</tr>
<tr>
<td>44</td>
<td></td>
<td>40</td>
<td>Start of the second blob. </td>
</tr>
</table>
 

The <b>WLAN_RAW_DATA_LIST</b> structure is currently used by the <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetpsdiedatalist">WlanSetPsdIEDataList</a> function to set the proximity service discovery (PSD) information element (IE) data list for an application. 

When used to store a PSD IE data list, the <b>DOT11_PSD_IE_MAX_ENTRY_NUMBER</b> constant defined in the <i>Wlanapi.h</i> header file is the maximum value of the <b>dwNumberOfItems</b> member for the number of blobs in the <b>WLAN_RAW_DATA_LIST</b> structure. The <b>DOT11_PSD_IE_MAX_DATA_SIZE</b> constant defined in the <i>Wlanapi.h</i> header file is the maximum value of the <b>dwDataSize</b> member for any blob.<table>
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
<tr>
<td><b>DOT11_PSD_IE_MAX_ENTRY_NUMBER</b></td>
<td>5</td>
<td>The maximum number of PSD IE data entries.</td>
</tr>
</table>
 



For more information about PSD IEs, including a discussion of the format of an IE, see <a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetpsdiedatalist">WlanSetPsdIEDataList</a>.

## -see-also

<a href="/windows/desktop/api/wlanapi/ns-wlanapi-wlan_raw_data">WLAN_RAW_DATA</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanextractpsdiedatalist">WlanExtractPsdIEDataList</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan">WlanScan</a>



<a href="/windows/desktop/api/wlanapi/nf-wlanapi-wlansetpsdiedatalist">WlanSetPsdIEDataList</a>