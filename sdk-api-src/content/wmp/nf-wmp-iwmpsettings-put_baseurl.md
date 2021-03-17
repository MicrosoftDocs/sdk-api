---
UID: NF:wmp.IWMPSettings.put_baseURL
title: IWMPSettings::put_baseURL (wmp.h)
description: The put_baseURL method specifies the base URL used for relative path resolution with URL script commands that are embedded in digital media files.
helpviewer_keywords: ["IWMPSettings interface [Windows Media Player]","put_baseURL method","IWMPSettings.put_baseURL","IWMPSettings::put_baseURL","IWMPSettingsput_baseURL","put_baseURL","put_baseURL method [Windows Media Player]","put_baseURL method [Windows Media Player]","IWMPSettings interface","wmp.iwmpsettings_put_baseurl","wmp/IWMPSettings::put_baseURL"]
old-location: wmp\iwmpsettings_put_baseurl.htm
tech.root: WMP
ms.assetid: ae070004-e90e-4f1e-b8b8-15deccdc48ad
ms.date: 12/05/2018
ms.keywords: IWMPSettings interface [Windows Media Player],put_baseURL method, IWMPSettings.put_baseURL, IWMPSettings::put_baseURL, IWMPSettingsput_baseURL, put_baseURL, put_baseURL method [Windows Media Player], put_baseURL method [Windows Media Player],IWMPSettings interface, wmp.iwmpsettings_put_baseurl, wmp/IWMPSettings::put_baseURL
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSettings::put_baseURL
 - wmp/IWMPSettings::put_baseURL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPSettings.put_baseURL
---

# IWMPSettings::put_baseURL


## -description

The <b>put_baseURL</b> method specifies the base URL used for relative path resolution with URL script commands that are embedded in digital media files.

## -parameters

### -param bstrBaseURL [in]

<b>BSTR</b> containing the base URL.

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
</table>

## -remarks

This method specifies the base HTTP URL that is passed as the command parameter by the <b>ScriptCommand</b> event. The base URL is concatenated with the relative URL as follows:

<ol>
<li>A trailing forward slash (/) is added to the value specified in the <b>put_baseURL</b> method.</li>
<li>A leading period, backward slash, or forward slash character (., \, and /) is deleted from the relative URL.</li>
<li>The relative URL is added to the end of the base URL.</li>
<li>All slash characters in the resulting fully qualified URL are pointed in the same direction (converted to forward or backward slashes) based on the direction of the first slash character encountered in the new URL.</li>
</ol>
<b>Note</b>

The Windows Media Player control does not support the use of two periods (..) in the relative URL to indicate the parent of the current location.

<b>Windows Media Player 10 Mobile: </b>This method always returns E_INVALIDARG.

## -see-also

<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents-scriptcommand">IWMPEvents::ScriptCommand</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsettings-get_baseurl">IWMPSettings::get_baseURL</a>