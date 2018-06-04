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

# IXDSToRat::ParseXDSBytePair


## -description




The <b>ParseXDSBytePair</b> method parses a single byte pair from an XDS stream. If the byte pair is the last pair in a completed ratings packet, the method returns the rating information.


## -parameters




### -param byte1 [in]

The first byte of the byte pair.


### -param byte2 [in]

The second byte of the byte pair.


### -param pEnSystem [out]

Receives the rating system, as a member of the <a href="https://msdn.microsoft.com/646927ad-569a-4484-a3ce-6d121210b6be">EnTvRat_System</a> enumeration type.


### -param pEnLevel [out]

Receives the rating level, as a member of the <a href="https://msdn.microsoft.com/f96a8f1a-d8e2-4976-92e3-719f0039d2a8">EnTvRat_GenericLevel</a> enumeration type. The meaning of this value depends on the rating system.


### -param plBfEnAttributes [out]

Receives a bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/eb7f56c4-1d48-43f9-a691-c08aee3cd537">BfEnTvRat_GenericAttributes</a> enumeration. These flags specify additional content attributes, such as violence or adult language. They do not apply to every rating system.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
No rating has been detected in the stream yet.

</td>
</tr>
</table>
 




## -remarks



The XDS Codec filter calls this method to pass XDS data to the <b>XDSToRat</b> object, one pair of bytes at a time. The <b>XDSToRat</b> object must store enough information between calls to be able to parse a complete ratings packet.

This method returns S_FALSE until the <b>XDSToRat</b> object decodes a complete ratings packet. At that point, the method returns S_OK and returns the rating information in the <i>pEnSystem</i>, <i>pEnLevel</i>, and <i>plBfEnAttributes</i> parameters. Subsequent calls return S_FALSE again until the next packet is decoded.

Ratings values may be delivered by either the XDS Content Advisory packet, or the Composite Packet-1 packet. For details, see sections 9.5.1.5 and 9.5.1.10, respectively, of the EIA/CEA-608B specification.

This method should also detect the Current Class Program Identificaton Number and Program Name packets indicating the end of show and return an S_OK value along with the values in the following table.

Return the following values for non-ratings packets.

<table>
<tr>
<th>
              Parameter
            </th>
<th>
              Value
            </th>
</tr>
<tr>
<td><i>pEnSystem</i></td>
<td><b>TvRat-SystemDontKnow</b></td>
</tr>
<tr>
<td><i>pEnLevel</i></td>
<td><b>TvRat_LevelDontKnow</b></td>
</tr>
<tr>
<td><i>plBfEnAttributes</i></td>
<td><b>BfAttrNone</b></td>
</tr>
</table>
 

For details, see section 9.5.1.5.4 (General Content Advisory Requirements) of the EIA/CEA-608-B specification.




## -see-also




<a href="https://msdn.microsoft.com/de65e5cd-3f4b-4925-a6b8-636fc2e332ec">IXDSToRat Interface</a>
 

 

