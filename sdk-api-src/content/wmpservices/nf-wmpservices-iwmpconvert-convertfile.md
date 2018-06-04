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

# IWMPConvert::ConvertFile


## -description



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




<a href="https://msdn.microsoft.com/316d1a13-0803-4414-8c51-0d5c4768b06d">IWMPConvert Interface</a>
 

 

