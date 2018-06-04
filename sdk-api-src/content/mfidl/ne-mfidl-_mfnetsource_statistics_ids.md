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

# _MFNETSOURCE_STATISTICS_IDS enumeration


## -description


Defines statistics collected by the network source. The values in this enumeration define property identifiers (PIDs) for the <a href="https://msdn.microsoft.com/1948481b-febd-434b-a5dc-faef592ea0ed">MFNETSOURCE_STATISTICS</a> property.

To retrieve statistics from the network source, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a> with the service identifier <b>MFNETSOURCE_STATISTICS_SERVICE</b> and the interface identifier IID_IPropertyStore. The retrieved pointer is an <b>IPropertyStore</b> pointer. To get the value of a network statistic, construct a <b>PROPERTYKEY</b> with <b>fmtid</b> equal to <b>MFNETSOURCE_STATISTICS</b> and <b>pid</b> equal to a value from this enumeration. Then call <b>IPropertyStore::GetValue</b> with the property key to retrieve the value of the statistic as a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>. 

In the descriptions that follow, the data type and value-type tag for the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> are listed in parentheses.


## -enum-fields




### -field MFNETSOURCE_RECVPACKETS_ID


            The number of packets received (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_LOSTPACKETS_ID


            The number of packets lost (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_RESENDSREQUESTED_ID


            The number of requests to resend packets (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_RESENDSRECEIVED_ID


            The number of resent packets received (<b>LONG</b>) (<b>VT_I4</b>).
          


### -field MFNETSOURCE_RECOVEREDBYECCPACKETS_ID


            The total number of packets recovered by error correction (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_RECOVEREDBYRTXPACKETS_ID


            The total number of packets recovered by retransmission (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_OUTPACKETS_ID


            The total number of packets returned to user, including recovered packets (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_RECVRATE_ID


            The 10-second average receiving rate (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_AVGBANDWIDTHBPS_ID


            The average bandwidth of the clip (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_BYTESRECEIVED_ID


            The total number of bytes received (<b>ULONGLONG</b>, <b>VT_UI8</b>).
          


### -field MFNETSOURCE_PROTOCOL_ID


            The type of control protocol used to receive the data (<b>LONG</b>, <b>VT_I4</b>). The value is a member of the <a href="https://msdn.microsoft.com/dd628b9e-3c52-4c14-aa0f-5e0b811d3f57">MFNETSOURCE_PROTOCOL_TYPE</a> enumeration.
          


### -field MFNETSOURCE_TRANSPORT_ID


            The type of control protocol used to receive the data (<b>LONG</b>, <b>VT_I4</b>). The value is a member of the <a href="https://msdn.microsoft.com/b3cdb604-15eb-4df7-af30-b21093c93781">MFNETSOURCE_TRANSPORT_TYPE</a> enumeration.
          


### -field MFNETSOURCE_CACHE_STATE_ID


            The status of cache for a media file or entry (<b>LONG</b>, <b>VT_I4</b>). The value is a member of the <a href="https://msdn.microsoft.com/fc7f2f66-02a3-455a-820b-304a53494ef1">MFNETSOURCE_CACHE_STATE</a> enumeration.
          


### -field MFNETSOURCE_LINKBANDWIDTH_ID


            The current link bandwidth, in bits per second (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_CONTENTBITRATE_ID


            The current bit rate of the content (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_SPEEDFACTOR_ID


            The negotiated speed factor used in data transmission (<b>LONG</b>, <b>VT_I4</b>). The sender transmits data at the rate of the speed factor multiplied by the bit rate of the content.
          


### -field MFNETSOURCE_BUFFERSIZE_ID


            The playout buffer size, in milliseconds (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_BUFFERPROGRESS_ID


            The percentage of the playout buffer filled during buffering. The value is an integer in the range 0–100. (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_LASTBWSWITCHTS_ID


            The number of ticks since the last bandwidth switch (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_SEEKRANGESTART_ID


            The start of the seekable range, in 100-nanosecond units (<b>ULONGLONG</b>, <b>VT_UI8</b>).
          


### -field MFNETSOURCE_SEEKRANGEEND_ID


            The end of the seekable range, in 100-nanosecond units (<b>ULONGLONG</b>, <b>VT_UI8</b>). 
          


### -field MFNETSOURCE_BUFFERINGCOUNT_ID


            The number of times buffering has occurred, including the initial buffering (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_INCORRECTLYSIGNEDPACKETS_ID


            The number of packets that had incorrect signatures (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_SIGNEDSESSION_ID


            Boolean value indicating whether the current session is signed (<b>VARIANT_BOOL</b>, <b>VT_BOOL</b>).
          


### -field MFNETSOURCE_MAXBITRATE_ID


            The current maximum bit rate of the content (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_RECEPTION_QUALITY_ID


            The reception quality (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_RECOVEREDPACKETS_ID


            The total number of recovered packets (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_VBR_ID


            Boolean value indicating whether the content has a variable bit rate (<b>VARIANT_BOOL</b>, <b>VT_BOOL</b>).
          


### -field MFNETSOURCE_DOWNLOADPROGRESS_ID


            The percentage of the content that has been downloaded. The value is an integer in the range 0–100.  (<b>LONG</b>, <b>VT_I4</b>).
          


### -field MFNETSOURCE_UNPREDEFINEDPROTOCOLNAME_ID




## -see-also




<a href="https://msdn.microsoft.com/f91b48ae-3989-4c1d-929c-8ab28d7c8177">Client Logging</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

