---
UID: NF:wmsdkidl.WMCreateLicenseRevocationAgent
title: WMCreateLicenseRevocationAgent function (wmsdkidl.h)
description: The WMCreateLicenseRevocationAgent function creates a license revocation object.
helpviewer_keywords: ["WMCreateLicenseRevocationAgent","WMCreateLicenseRevocationAgent function [windows Media Format]","wmformat.wmcreatelicenserevocationagent","wmsdkidl/WMCreateLicenseRevocationAgent"]
old-location: wmformat\wmcreatelicenserevocationagent.htm
tech.root: wmformat
ms.assetid: 46898846-780f-4a86-93c7-826f55c358ba
ms.date: 4/26/2023
ms.keywords: WMCreateLicenseRevocationAgent, WMCreateLicenseRevocationAgent function [windows Media Format], wmformat.wmcreatelicenserevocationagent, wmsdkidl/WMCreateLicenseRevocationAgent
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMCreateLicenseRevocationAgent
 - wmsdkidl/WMCreateLicenseRevocationAgent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateLicenseRevocationAgent
---

# WMCreateLicenseRevocationAgent function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WMCreateLicenseRevocationAgent</b> function creates a license revocation object.

## -parameters

### -param pCallback [in]

Address of the <b>IUnknown</b> interface of the object that implements the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback method used to communicate license revocation status to the application.

### -param ppLicenseRevocationAgent [out]

Address of a variable that receives a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserevocationagent">IWMLicenseRevocationAgent</a> interface of the newly created license revocation agent object.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The function succeeded.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>The function is unable to allocate memory for the new object.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/functions">Functions</a>