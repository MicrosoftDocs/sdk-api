---
UID: NF:wincodec.IWICProgressiveLevelControl.SetCurrentLevel
title: IWICProgressiveLevelControl::SetCurrentLevel
author: windows-sdk-content
description: Specifies the level to retrieve on the next call to CopyPixels.
old-location: wic\_wic_codec_iwicprogressivelevelcontrol_setcurrentlevel.htm
tech.root: wic
ms.assetid: b4a2c279-385d-4177-bd8f-a49f545c692a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWICProgressiveLevelControl interface [Windows Imaging Component],SetCurrentLevel method, IWICProgressiveLevelControl.SetCurrentLevel, IWICProgressiveLevelControl::SetCurrentLevel, SetCurrentLevel, SetCurrentLevel method [Windows Imaging Component], SetCurrentLevel method [Windows Imaging Component],IWICProgressiveLevelControl interface, _wic_codec_iwicprogressivelevelcontrol_setcurrentlevel, wic._wic_codec_iwicprogressivelevelcontrol_setcurrentlevel, wincodec/IWICProgressiveLevelControl::SetCurrentLevel
ms.topic: method
req.header: wincodec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wincodec.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Windowscodecs.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICProgressiveLevelControl.SetCurrentLevel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

