---
UID: NF:bits3_0.IBitsPeerCacheRecord.GetOriginUrl
title: IBitsPeerCacheRecord::GetOriginUrl (bits3_0.h)
author: windows-sdk-content
description: Gets the origin URL of the cached file.
old-location: bits\ibitspeercacherecord_getoriginurl.htm
tech.root: Bits
ms.assetid: 9d74df3a-89e0-4a3a-82f3-c2e79c609b21
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetOriginUrl, GetOriginUrl method [BITS], GetOriginUrl method [BITS],IBitsPeerCacheRecord interface, IBitsPeerCacheRecord interface [BITS],GetOriginUrl method, IBitsPeerCacheRecord.GetOriginUrl, IBitsPeerCacheRecord::GetOriginUrl, bits.ibitspeercacherecord_getoriginurl, bits3_0/IBitsPeerCacheRecord::GetOriginUrl
ms.topic: method
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBitsPeerCacheRecord.GetOriginUrl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBitsPeerCacheRecord::GetOriginUrl


## -description


Gets the origin URL of the cached file.


## -parameters




### -param pVal [in]

Null-terminated string that contains the origin URL of the cached file. Call the 
<a href="https://msdn.microsoft.com/en-us/library/windows/desktop/ms680722">CoTaskMemFree</a> function to free <i>ppOriginUrl</i> when done.


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -remarks



This URL may be different than the URL originally specified in the BITS job if <a href="https://msdn.microsoft.com/afac84cb-28ab-4c80-ab39-eefe450ae3e5">IBackgroundCopyJobHttpOptions::SetSecurityFlags</a> is set to BG_HTTP_REDIRECT_POLICY_ALLOW_REPORT or BG_HTTP_REDIRECT_POLICY_DISALLOW.




## -see-also




<a href="https://msdn.microsoft.com/61db33de-a38c-4c52-9f1b-66d46f25c297">IBitsPeerCacheRecord</a>
 

 

