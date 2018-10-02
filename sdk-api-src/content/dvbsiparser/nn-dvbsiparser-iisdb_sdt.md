---
UID: NN:dvbsiparser.IISDB_SDT
title: IISDB_SDT
author: windows-sdk-content
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) service description table (SDT). An SDT lists the names and other parameters of the services in an MPEG-2 transport stream.
old-location: mstv\iisdb_sdt.htm
tech.root: MSTV
ms.assetid: a9824eb9-ec12-4a09-ba42-243fe19c0670
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IISDB_SDT, IISDB_SDT interface [Microsoft TV Technologies], IISDB_SDT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_SDT, mstv.iisdb_sdt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IISDB_SDT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IISDB_SDT interface


## -description


Implements methods that get information from an Integrated Services Digital Broadcasting
  (ISDB)
  service description table (SDT). An SDT
  lists the names and other parameters of the services in an MPEG-2 transport stream.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an SDT. Then:

<ol>
<li>Query the <a href="https://msdn.microsoft.com/22044a4c-480f-4c98-a78e-52c66a5eac99">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="https://msdn.microsoft.com/6f07b4d2-7a52-448c-9e9f-729bd5261757">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="https://msdn.microsoft.com/4b2362c7-bfcb-40b8-813d-1a904149600e">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IISDB_SDT</b> interface inherits from <a href="https://msdn.microsoft.com/bb473a7e-8957-4e85-98d0-13c6992fbf37">IDVB_SDT</a>. <b>IISDB_SDT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IISDB_SDT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c67d37e5-f258-45f5-8bc7-c539e3fa5e1a">GetRecordEITUserDefinedFlags</a>
</td>
<td align="left" width="63%">
Returns the EIT_user_defined_flags field value from an SDT.

</td>
</tr>
</table> 

