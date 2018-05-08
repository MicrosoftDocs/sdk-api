---
UID: NE:mfidl._MFNETSOURCE_STATISTICS_IDS
title: "_MFNETSOURCE_STATISTICS_IDS"
author: windows-driver-content
description: Defines statistics collected by the network source.
old-location: mf\mfnetsource_statistics_ids.htm
old-project: medfound
ms.assetid: 4956e003-7f52-40af-8f6b-b1b73ba2a897
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: 4956e003-7f52-40af-8f6b-b1b73ba2a897, MFNETSOURCE_AVGBANDWIDTHBPS_ID, MFNETSOURCE_BUFFERINGCOUNT_ID, MFNETSOURCE_BUFFERPROGRESS_ID, MFNETSOURCE_BUFFERSIZE_ID, MFNETSOURCE_BYTESRECEIVED_ID, MFNETSOURCE_CACHE_STATE_ID, MFNETSOURCE_CONTENTBITRATE_ID, MFNETSOURCE_DOWNLOADPROGRESS_ID, MFNETSOURCE_INCORRECTLYSIGNEDPACKETS_ID, MFNETSOURCE_LASTBWSWITCHTS_ID, MFNETSOURCE_LINKBANDWIDTH_ID, MFNETSOURCE_LOSTPACKETS_ID, MFNETSOURCE_MAXBITRATE_ID, MFNETSOURCE_OUTPACKETS_ID, MFNETSOURCE_PROTOCOL_ID, MFNETSOURCE_RECEPTION_QUALITY_ID, MFNETSOURCE_RECOVEREDBYECCPACKETS_ID, MFNETSOURCE_RECOVEREDBYRTXPACKETS_ID, MFNETSOURCE_RECOVEREDPACKETS_ID, MFNETSOURCE_RECVPACKETS_ID, MFNETSOURCE_RECVRATE_ID, MFNETSOURCE_RESENDSRECEIVED_ID, MFNETSOURCE_RESENDSREQUESTED_ID, MFNETSOURCE_SEEKRANGEEND_ID, MFNETSOURCE_SEEKRANGESTART_ID, MFNETSOURCE_SIGNEDSESSION_ID, MFNETSOURCE_SPEEDFACTOR_ID, MFNETSOURCE_STATISTICS_IDS, MFNETSOURCE_STATISTICS_IDS enumeration [Media Foundation], MFNETSOURCE_TRANSPORT_ID, MFNETSOURCE_VBR_ID, _MFNETSOURCE_STATISTICS_IDS, mf.mfnetsource_statistics_ids, mfidl/MFNETSOURCE_AVGBANDWIDTHBPS_ID, mfidl/MFNETSOURCE_BUFFERINGCOUNT_ID, mfidl/MFNETSOURCE_BUFFERPROGRESS_ID, mfidl/MFNETSOURCE_BUFFERSIZE_ID, mfidl/MFNETSOURCE_BYTESRECEIVED_ID, mfidl/MFNETSOURCE_CACHE_STATE_ID, mfidl/MFNETSOURCE_CONTENTBITRATE_ID, mfidl/MFNETSOURCE_DOWNLOADPROGRESS_ID, mfidl/MFNETSOURCE_INCORRECTLYSIGNEDPACKETS_ID, mfidl/MFNETSOURCE_LASTBWSWITCHTS_ID, mfidl/MFNETSOURCE_LINKBANDWIDTH_ID, mfidl/MFNETSOURCE_LOSTPACKETS_ID, mfidl/MFNETSOURCE_MAXBITRATE_ID, mfidl/MFNETSOURCE_OUTPACKETS_ID, mfidl/MFNETSOURCE_PROTOCOL_ID, mfidl/MFNETSOURCE_RECEPTION_QUALITY_ID, mfidl/MFNETSOURCE_RECOVEREDBYECCPACKETS_ID, mfidl/MFNETSOURCE_RECOVEREDBYRTXPACKETS_ID, mfidl/MFNETSOURCE_RECOVEREDPACKETS_ID, mfidl/MFNETSOURCE_RECVPACKETS_ID, mfidl/MFNETSOURCE_RECVRATE_ID, mfidl/MFNETSOURCE_RESENDSRECEIVED_ID, mfidl/MFNETSOURCE_RESENDSREQUESTED_ID, mfidl/MFNETSOURCE_SEEKRANGEEND_ID, mfidl/MFNETSOURCE_SEEKRANGESTART_ID, mfidl/MFNETSOURCE_SIGNEDSESSION_ID, mfidl/MFNETSOURCE_SPEEDFACTOR_ID, mfidl/MFNETSOURCE_STATISTICS_IDS, mfidl/MFNETSOURCE_TRANSPORT_ID, mfidl/MFNETSOURCE_VBR_ID
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFNETSOURCE_STATISTICS_IDS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfidl.h
api_name:
-	MFNETSOURCE_STATISTICS_IDS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

