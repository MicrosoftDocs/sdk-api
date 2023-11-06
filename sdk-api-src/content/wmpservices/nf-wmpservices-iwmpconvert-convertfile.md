---
UID: NF:wmpservices.IWMPConvert.ConvertFile
title: IWMPConvert::ConvertFile (wmpservices.h)
description: The ConvertFile method is implemented by a conversion plug-in and called by Windows Media Player to enable a conversion plug-in to convert a digital media file into ASF.
helpviewer_keywords: ["ConvertFile","ConvertFile method [Windows Media Player]","ConvertFile method [Windows Media Player]","IWMPConvert interface","IWMPConvert interface [Windows Media Player]","ConvertFile method","IWMPConvert.ConvertFile","IWMPConvert::ConvertFile","IWMPConvertConvertFile","wmp.iwmpconvert_convertfile","wmpservices/IWMPConvert::ConvertFile"]
old-location: wmp\iwmpconvert_convertfile.htm
tech.root: WMP
ms.assetid: 69ca3863-94ec-457f-9f93-aebb5b80c8a9
ms.date: 4/26/2023
ms.keywords: ConvertFile, ConvertFile method [Windows Media Player], ConvertFile method [Windows Media Player],IWMPConvert interface, IWMPConvert interface [Windows Media Player],ConvertFile method, IWMPConvert.ConvertFile, IWMPConvert::ConvertFile, IWMPConvertConvertFile, wmp.iwmpconvert_convertfile, wmpservices/IWMPConvert::ConvertFile
req.header: wmpservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player, build 10.00.00.4521 or later
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPConvert::ConvertFile
 - wmpservices/IWMPConvert::ConvertFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmpservices.h
api_name:
 - IWMPConvert.ConvertFile
---

# IWMPConvert::ConvertFile


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>ConvertFile</b> method is implemented by a conversion plug-in and called by Windows Media Player to enable a conversion plug-in to convert a digital media file into ASF.

## -parameters

### -param bstrInputFile [in]

<b>BSTR</b> containing the path to the file to be converted.

### -param bstrDestinationFolder [in]

<b>BSTR</b> containing that path to the folder where the converted file must be copied.

### -param pbstrOutputFile [out]

Pointer to a <b>BSTR</b> that receives the path to the converted file.

## -returns

The method returns an <b>HRESULT</b>. The following table lists recommended return codes.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_FILE_FAILED</b></dt>
<dt>0xC00D1158</dt>
</dl>
</td>
<td width="60%">
Unspecified failure while converting the file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_NO_RIGHTS_ERRORURL</b></dt>
<dt>0xC00D1159</dt>
</dl>
</td>
<td width="60%">
The license prohibits file conversion. <b>IWMPConvert::GetErrorURL</b> must return the URL of the webpage that describes the issue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_NO_RIGHTS_NOERRORURL</b></dt>
<dt>0xC00D115A</dt>
</dl>
</td>
<td width="60%">
The license prohibits file conversion. There is no error URL available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_FILE_CORRUPT</b></dt>
<dt>0xC00D115B</dt>
</dl>
</td>
<td width="60%">
The specified file is corrupted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_PLUGIN_UNAVAILABLE_ERRORURL</b></dt>
<dt>0xC00D115C</dt>
</dl>
</td>
<td width="60%">
There is an unspecified problem with the plug-in. <b>IWMPConvert::GetErrorURL</b> must return the URL of the webpage where the user can reinstall the plug-in.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_PLUGIN_UNAVAILABLE_NOERRORURL</b></dt>
<dt>0xC00D115D</dt>
</dl>
</td>
<td width="60%">
There is an unspecified problem with the plug-in. There is no error URL available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_WMP_CONVERT_PLUGIN_UNKNOWN_FILE_OWNER</b></dt>
<dt>0xC00D115E</dt>
</dl>
</td>
<td width="60%">
This conversion plug-in is not the correct one to convert the current file.

</td>
</tr>
</table>

## -remarks

This is a synchronous call. Your code must complete and return as quickly as possible. This method is not intended to be used for transcoding digital media files. You should use this method only to change the file format.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.

## -see-also

<a href="/windows/desktop/api/wmpservices/nn-wmpservices-iwmpconvert">IWMPConvert Interface</a>