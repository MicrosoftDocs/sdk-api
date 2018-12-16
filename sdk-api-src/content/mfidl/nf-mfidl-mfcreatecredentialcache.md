---
UID: NF:mfidl.MFCreateCredentialCache
title: MFCreateCredentialCache function
author: windows-sdk-content
description: Creates a credential cache object. An application can use this object to implement a custom credential manager.
old-location: mf\mfcreatecredentialcache.htm
tech.root: medfound
ms.assetid: ec27f54a-4534-4342-856b-f6f55c5a7fdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MFCreateCredentialCache, MFCreateCredentialCache function [Media Foundation], ec27f54a-4534-4342-856b-f6f55c5a7fdb, mf.mfcreatecredentialcache, mfidl/MFCreateCredentialCache
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateCredentialCache
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateCredentialCache function


## -description



Creates a credential cache object. An application can use this object to implement a custom credential manager.




## -parameters




### -param ppCache

Receives a pointer to the <a href="https://msdn.microsoft.com/d02e26e7-e99c-4be7-8495-830eff2f1554">IMFNetCredentialCache</a> interface of the new credential cache object. The caller must release the interface.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d02e26e7-e99c-4be7-8495-830eff2f1554">IMFNetCredentialCache</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

