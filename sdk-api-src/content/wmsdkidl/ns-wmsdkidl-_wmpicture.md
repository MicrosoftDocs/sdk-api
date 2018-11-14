---
UID: NS:wmsdkidl._WMPicture
title: "_WMPicture"
author: windows-sdk-content
description: The WM_PICTURE structure is used as the data item for the WM/Picture complex metadata attribute.
old-location: wmformat\wm_picture.htm
tech.root: wmformat
ms.assetid: d3670cce-5b57-4624-b10d-2e4d9e9e263c
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: WM_PICTURE, WM_PICTURE structure [windows Media Format], _WMPicture, wmformat.wm_picture, wmsdkidl/WM_PICTURE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_PICTURE
product: Windows
targetos: Windows
req.typenames: WM_PICTURE
req.redist: 
---

# _WMPicture structure


## -description



The <b>WM_PICTURE</b> structure is used as the data item for the <a href="https://msdn.microsoft.com/ec82dfdf-7755-4758-9771-096aac114f78">WM/Picture</a> complex metadata attribute.




## -struct-fields




### -field pwszMIMEType

Pointer to a wide-character null-terminated string containing the multipurpose Internet mail extension (MIME) type of the picture.


### -field bPictureType

<b>BYTE</b> value containing one of the following values.<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>0</td>
<td>Picture of a type not specifically listed in this table</td>
</tr>
<tr>
<td>1</td>
<td>32 pixel by 32 pixel file icon. Use only with portable network graphics (PNG) format</td>
</tr>
<tr>
<td>2</td>
<td>File icon not conforming to type 1 above</td>
</tr>
<tr>
<td>3</td>
<td>Front album cover</td>
</tr>
<tr>
<td>4</td>
<td>Back album cover</td>
</tr>
<tr>
<td>5</td>
<td>Leaflet page</td>
</tr>
<tr>
<td>6</td>
<td>Media. Typically this type of image is of the label side of a CD</td>
</tr>
<tr>
<td>7</td>
<td>Picture of the lead artist, lead performer, or soloist</td>
</tr>
<tr>
<td>8</td>
<td>Picture of one of the artists or performers</td>
</tr>
<tr>
<td>9</td>
<td>Picture of the conductor</td>
</tr>
<tr>
<td>10</td>
<td>Picture of the band or orchestra</td>
</tr>
<tr>
<td>11</td>
<td>Picture of the composer</td>
</tr>
<tr>
<td>12</td>
<td>Picture of the lyricist or writer</td>
</tr>
<tr>
<td>13</td>
<td>Picture of the recording studio or location</td>
</tr>
<tr>
<td>14</td>
<td>Picture taken during a recording session</td>
</tr>
<tr>
<td>15</td>
<td>Picture taken during a performance</td>
</tr>
<tr>
<td>16</td>
<td>Screen capture from a movie or video</td>
</tr>
<tr>
<td>17</td>
<td>A bright colored fish</td>
</tr>
<tr>
<td>18</td>
<td>Illustration</td>
</tr>
<tr>
<td>19</td>
<td>Logo of the band or artist</td>
</tr>
<tr>
<td>20</td>
<td>Logo of the publisher or studio</td>
</tr>
</table>
 




### -field pwszDescription

Pointer to a wide-character null-terminated string containing a description of the picture.


### -field dwDataLen

<b>DWORD</b> value containing the size, in bytes, of the picture data pointed to by <b>pbData</b>.


### -field pbData

Pointer to a <b>BYTE</b> array containing the picture data.


## -see-also




<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

