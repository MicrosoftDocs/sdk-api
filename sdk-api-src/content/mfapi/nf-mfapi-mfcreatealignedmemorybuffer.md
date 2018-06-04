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

# MFCreateAlignedMemoryBuffer function


## -description



          Allocates system memory with a specified byte alignment and creates a media buffer to manage the memory.
        


## -parameters




### -param cbMaxLength

Size of the buffer, in bytes.


### -param cbAligment

TBD


### -param ppBuffer


            Receives a pointer to the <a href="https://msdn.microsoft.com/3ccc7089-d0d0-4eb1-b763-0d4e348af685">IMFMediaBuffer</a> interface of the media buffer. The caller must release the interface.
          


#### - fAlignmentFlags


            Specifies the memory alignment for the buffer. Use one of the following constants.
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MF_1_BYTE_ALIGNMENT"></a><a id="mf_1_byte_alignment"></a><dl>
<dt><b>MF_1_BYTE_ALIGNMENT</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">

                Align to 1 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_2_BYTE_ALIGNMENT"></a><a id="mf_2_byte_alignment"></a><dl>
<dt><b>MF_2_BYTE_ALIGNMENT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">

                Align to 2 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_4_BYTE_ALIGNMENT"></a><a id="mf_4_byte_alignment"></a><dl>
<dt><b>MF_4_BYTE_ALIGNMENT</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">

                Align to 4 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_8_BYTE_ALIGNMENT"></a><a id="mf_8_byte_alignment"></a><dl>
<dt><b>MF_8_BYTE_ALIGNMENT</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">

                Align to 8 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_16_BYTE_ALIGNMENT"></a><a id="mf_16_byte_alignment"></a><dl>
<dt><b>MF_16_BYTE_ALIGNMENT</b></dt>
<dt>0x0000000F</dt>
</dl>
</td>
<td width="60%">

                Align to 16 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_32_BYTE_ALIGNMENT"></a><a id="mf_32_byte_alignment"></a><dl>
<dt><b>MF_32_BYTE_ALIGNMENT</b></dt>
<dt>0x0000001F</dt>
</dl>
</td>
<td width="60%">

                Align to 32 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_64_BYTE_ALIGNMENT"></a><a id="mf_64_byte_alignment"></a><dl>
<dt><b>MF_64_BYTE_ALIGNMENT</b></dt>
<dt>0x0000003F</dt>
</dl>
</td>
<td width="60%">

                Align to 64 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_128_BYTE_ALIGNMENT"></a><a id="mf_128_byte_alignment"></a><dl>
<dt><b>MF_128_BYTE_ALIGNMENT</b></dt>
<dt>0x0000007F</dt>
</dl>
</td>
<td width="60%">

                Align to 128 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_256_BYTE_ALIGNMENT"></a><a id="mf_256_byte_alignment"></a><dl>
<dt><b>MF_256_BYTE_ALIGNMENT</b></dt>
<dt>0x000000FF</dt>
</dl>
</td>
<td width="60%">

                Align to 256 bytes.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MF_512_BYTE_ALIGNMENT"></a><a id="mf_512_byte_alignment"></a><dl>
<dt><b>MF_512_BYTE_ALIGNMENT</b></dt>
<dt>0x000001FF</dt>
</dl>
</td>
<td width="60%">

                Align to 512 bytes.
              

</td>
</tr>
</table>
 


## -returns




            The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">

                The function succeeded.
              

</td>
</tr>
</table>
 




## -remarks




        When the media buffer object is destroyed, it releases the allocated memory.
      




## -see-also




<a href="https://msdn.microsoft.com/1f79d057-7ef7-4662-9f82-ceadc23276f0">MFCreateMemoryBuffer</a>



<a href="https://msdn.microsoft.com/3ee073ea-7bac-4971-9167-93a4e541ab77">Media Buffers</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

