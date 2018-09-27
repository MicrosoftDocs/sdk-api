---
UID: NF:wlanapi.WlanExtractPsdIEDataList
title: WlanExtractPsdIEDataList function
author: windows-sdk-content
description: Extracts the proximity service discovery (PSD) information element (IE) data list from raw IE data included in a beacon.
old-location: nwifi\wlanextractpsdiedatalist.htm
tech.root: NativeWiFi
ms.assetid: 7fb6707f-c229-4386-9058-e290693a20ce
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WlanExtractPsdIEDataList, WlanExtractPsdIEDataList function [NativeWIFI], nwifi.wlanextractpsdiedatalist, wlanapi/WlanExtractPsdIEDataList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanExtractPsdIEDataList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WlanExtractPsdIEDataList function


## -description


The <b>WlanExtractPsdIEDataList</b> function extracts the proximity service discovery (PSD) information element (IE) data list from raw IE data included in a beacon.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param dwIeDataSize [in]

The size, in bytes, of the <i>pRawIeData</i> parameter.


### -param pRawIeData [in]

The raw IE data for all IEs in the list.


### -param strFormat [in]

Describes the format of a PSD IE. Only IEs with a matching format are returned.


### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.


### -param ppPsdIEDataList [out]

A pointer to a <a href="https://msdn.microsoft.com/e0e59abf-1a78-4c7f-b044-2d4c75328329">PWLAN_RAW_DATA_LIST</a> structure that contains the formatted data list.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid, <i>dwIeDataSize</i> is 0, <i>pRawIeData</i> is <b>NULL</b>, or <i>pReserved</i> is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function was called from an unsupported platform. This value will be returned if this function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
</table>
 




## -remarks



For more information about PSD IEs, including a discussion of the format of an IE, see <a href="https://msdn.microsoft.com/eea402d3-9a5f-4446-bf6c-9ab8430f9c60">WlanSetPsdIEDataList</a>.




## -see-also




<a href="https://msdn.microsoft.com/e0e59abf-1a78-4c7f-b044-2d4c75328329">WLAN_RAW_DATA_LIST</a>



<a href="https://msdn.microsoft.com/eea402d3-9a5f-4446-bf6c-9ab8430f9c60">WlanSetPsdIEDataList</a>
 

 

