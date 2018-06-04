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

# IOfflineFilesCache::GetEncryptionStatus


## -description


Retrieves the current encryption state (encrypted or unencrypted) of the Offline Files cache.


## -parameters




### -param pbEncrypted [out]

Receives <b>TRUE</b> if the Offline Files cache is configured to be encrypted; <b>FALSE</b> if configured to be unencrypted.


### -param pbPartial [out]

Receives <b>TRUE</b> if the Offline Files cache is partially encrypted or partially unencrypted based on the value returned in <i>pbEncrypted</i>; <b>FALSE</b> if it is fully encrypted or unencrypted.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



This encryption state is read from the Offline Files cache and reflects the state of the cache at that instant.

This method returns two values that indicate if the cache is fully encrypted, partially encrypted, fully unencrypted or partially unencrypted.

To change the encryption state of the cache, use the <a href="https://msdn.microsoft.com/b7531018-4837-4fde-8947-0f099f6de9e5">IOfflineFilesCache::Encrypt</a> method.


#### Examples

The following example shows how to use this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>    //
    // Assume we already have a cache ptr.
    //
    IOfflineFilesCache *pCache;
    BOOL bEncrypted;
    BOOL bPartial;
    HRESULT hr = pCache-&gt;GetEncryptionStatus(&amp;bEncrypted, &amp;bPartial);
    if (SUCCEEDED(hr))
    {
        if (bEncrypted)
        {
            if (bPartial)
            {
                // Cache is partially encrypted.
            }
            else
            {
                // Cache is fully encrypted.
            }
        }
        else
        {
            if (bPartial)
            {
                // Cache is partially unencrypted.
            }
            else
            {
                // Cache is fully unencrypted.
            }
        }
    }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
 

 

