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

# IWICProgressiveLevelControl::SetCurrentLevel


## -description


Specifies the level to retrieve on the next call to <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a>.


## -parameters




### -param nLevel [in]

Type: <b>UINT</b>

Specifies which level to return next. If greater than the total number of levels supported, an error will be returned.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        A call does not have to request every level supported.
        If a caller requests level 1, without having previously requested level 0, the bits returned by the next call to <a href="https://msdn.microsoft.com/d4908a75-e7de-4b8f-bdc8-d86cf6b49f8c">CopyPixels</a> will include both levels.
      


         
If the requested level is invalid, the error returned is <a href="https://msdn.microsoft.com/1ded909c-311b-49e3-ba23-b22cd7a77bc6">WINCODEC_ERR_INVALIDPROGRESSIVELEVEL</a>.


#### Examples

Users should use this method to iterate through the progressive levels of a progressive JPEG image rather than the <a href="https://msdn.microsoft.com/c6f848a0-e373-4344-8923-3ad77165ef71">GetCurrentLevel</a> method. JPEG progressive levels are determined by the image and do not have a fixed level count. 
         Using <b>GetCurrentLevel</b> method will force the application to wait for all progressive levels to be downloaded before it can return. 
         Instead, applications should use the following code to iterate through the progressive levels of a progressive JPEG image.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame-&gt;QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &amp;pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive-&gt;SetCurrentLevel(uCurrentLevel);
      if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame-&gt;CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive-&gt;Release();
}	
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d77244bc-b9d4-4b7d-b718-4ee38de46614">IWICProgressiveLevelControl</a>



<a href="https://msdn.microsoft.com/d22c2c59-0fa1-4452-93f1-dbf151033714">Progressive Decoding Overview</a>
 

 

