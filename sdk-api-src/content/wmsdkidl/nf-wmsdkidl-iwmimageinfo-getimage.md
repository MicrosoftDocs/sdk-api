---
UID: NF:wmsdkidl.IWMImageInfo.GetImage
title: IWMImageInfo::GetImage (wmsdkidl.h)
description: The GetImage method retrieves an image stored in a file as an ID3v2 &#0034;APIC&#0034; metadata frame.
helpviewer_keywords: ["GetImage","GetImage method [windows Media Format]","GetImage method [windows Media Format]","IWMImageInfo interface","IWMImageInfo interface [windows Media Format]","GetImage method","IWMImageInfo.GetImage","IWMImageInfo::GetImage","IWMImageInfoGetImage","wmformat.iwmimageinfo_getimage","wmsdkidl/IWMImageInfo::GetImage"]
old-location: wmformat\iwmimageinfo_getimage.htm
tech.root: wmformat
ms.assetid: fe1dcd53-fcdd-4190-9a07-65d0b34112d0
ms.date: 4/26/2023
ms.keywords: GetImage, GetImage method [windows Media Format], GetImage method [windows Media Format],IWMImageInfo interface, IWMImageInfo interface [windows Media Format],GetImage method, IWMImageInfo.GetImage, IWMImageInfo::GetImage, IWMImageInfoGetImage, wmformat.iwmimageinfo_getimage, wmsdkidl/IWMImageInfo::GetImage
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMImageInfo::GetImage
 - wmsdkidl/IWMImageInfo::GetImage
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMImageInfo.GetImage
---

# IWMImageInfo::GetImage


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetImage</b> method retrieves an image stored in a file as an ID3v2 "APIC" metadata frame.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the image index. This is a number between zero, and one less than the image count retrieved by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmimageinfo-getimagecount">IWMImageInfo::GetImageCount</a>.

### -param pcchMIMEType [in, out]

Pointer to a <b>WORD</b> containing the length, in wide characters, of <i>pwszMIMEType</i>, including the terminating <b>NULL</b> character. On the first call to this method, pass <b>NULL</b> as <i>pwszMIMEType</i> to retrieve the required number of characters.

### -param pwszMIMEType [out]

Pointer to a wide-character <b>null</b>-terminated string containing the MIME Type associated with the image. Set to <b>NULL</b> on the first call and <i>pcchMIMEType</i> will be set to the number of wide characters, including the terminating <b>NULL</b>, in this string.

### -param pcchDescription [in, out]

Pointer to a <b>WORD</b> containing the length, in wide characters, of <i>pwszDescription</i>, including the terminating <b>NULL</b> character. On the first call to this method, pass <b>NULL</b> as <i>pwszDescription</i> to retrieve the required number of characters.

### -param pwszDescription [out]

Pointer to a wide-character <b>null</b>-terminated string containing the image description. Set to <b>NULL</b> on the first call and <i>pcchDescription</i> will be set to the number of wide characters, including the terminating <b>NULL</b>, in this string.

### -param pImageType [out]

Pointer to a <b>WORD</b> value containing the image type, as defined by the ID3v2 specification. This will be one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>0</td>
<td>Picture of a type not specifically listed in this table</td>
</tr>
<tr>
<td>1</td>
<td>32-pixel-by-32-pixel file icon. Use only with portable network graphics (PNG) format.</td>
</tr>
<tr>
<td>2</td>
<td>File icon not conforming to type 1 above.</td>
</tr>
<tr>
<td>3</td>
<td>Front album cover.</td>
</tr>
<tr>
<td>4</td>
<td>Back album cover.</td>
</tr>
<tr>
<td>5</td>
<td>Leaflet page.</td>
</tr>
<tr>
<td>6</td>
<td>Media. Typically this type of image is of the label side of a CD.</td>
</tr>
<tr>
<td>7</td>
<td>Picture of the lead artist, lead performer, or soloist.</td>
</tr>
<tr>
<td>8</td>
<td>Picture of one of the involved artists or performers.</td>
</tr>
<tr>
<td>9</td>
<td>Picture of the conductor.</td>
</tr>
<tr>
<td>10</td>
<td>Picture of the band or orchestra.</td>
</tr>
<tr>
<td>11</td>
<td>Picture of the composer.</td>
</tr>
<tr>
<td>12</td>
<td>Picture of the lyricist or writer.</td>
</tr>
<tr>
<td>13</td>
<td>Picture of the recording studio or location.</td>
</tr>
<tr>
<td>14</td>
<td>Picture taken during a recording session.</td>
</tr>
<tr>
<td>15</td>
<td>Picture taken during a performance.</td>
</tr>
<tr>
<td>16</td>
<td>Screen capture from a movie or video.</td>
</tr>
<tr>
<td>17</td>
<td>A bright colored fish.</td>
</tr>
<tr>
<td>18</td>
<td>Illustration.</td>
</tr>
<tr>
<td>19</td>
<td>Logo of the band or artist.</td>
</tr>
<tr>
<td>20</td>
<td>Logo of the publisher or studio.</td>
</tr>
</table>

### -param pcbImageData [in, out]

Pointer to a <b>DWORD</b> containing the length, in bytes, of the image pointed to by <i>pbImageData</i>. On the first call to this method, pass <b>NULL</b> as <i>pbImageData</i> to retrieve the required number of bytes.

### -param pbImageData [out]

Pointer to a <b>BYTE</b> buffer containing the image data. Set to <b>NULL</b> on the first call and <i>pcbImageData</i> will be set to the number of bytes in the buffer.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more of the following parameters is <b>NULL</b>.

<i>pcchMIMEType</i>

<b><i></i></b>

<i>pcbImageData</i>

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
One of the ID3 frames that should be in the file cannot be accessed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The value referenced by one of the following parameters is less than the required buffer size for the corresponding output parameter.

<i>pcchMIMEType</i>

<i>pcchDescription</i>

<i>pcbImageData</i>

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmimageinfo-getimagecount">GetImageCount</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo">IWMImageInfo Interface</a>