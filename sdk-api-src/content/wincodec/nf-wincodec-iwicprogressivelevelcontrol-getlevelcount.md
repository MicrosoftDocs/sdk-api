---
UID: NF:wincodec.IWICProgressiveLevelControl.GetLevelCount
title: IWICProgressiveLevelControl::GetLevelCount
author: windows-sdk-content
description: Gets the number of levels of progressive decoding supported by the CODEC.
old-location: wic\_wic_codec_iwicprogressivelevelcontrol_getlevelcount.htm
tech.root: wic
ms.assetid: f7949d31-c679-43ea-aa07-5f9f8579b4f7
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetLevelCount, GetLevelCount method [Windows Imaging Component], GetLevelCount method [Windows Imaging Component],IWICProgressiveLevelControl interface, IWICProgressiveLevelControl interface [Windows Imaging Component],GetLevelCount method, IWICProgressiveLevelControl.GetLevelCount, IWICProgressiveLevelControl::GetLevelCount, _wic_codec_iwicprogressivelevelcontrol_getlevelcount, wic._wic_codec_iwicprogressivelevelcontrol_getlevelcount, wincodec/IWICProgressiveLevelControl::GetLevelCount
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWICProgressiveLevelControl.GetLevelCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWICProgressiveLevelControl::GetLevelCount


## -description


Gets the number of levels of progressive decoding supported by the CODEC.


## -parameters




### -param pcLevels [out, retval]

Type: <b>UINT*</b>

Indicates the number of levels supported by the CODEC.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Users should not use this function to iterate through the progressive levels of a progressive JPEG image. JPEG progressive levels are determined by the image and do not have a fixed level count. Using this method will force the application to wait for all progressive levels to be downloaded before it can return. Instead, applications should use the following code to iterate through the progressive levels of a progressive JPEG image.


#### Examples

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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d77244bc-b9d4-4b7d-b718-4ee38de46614">IWICProgressiveLevelControl</a>



<a href="https://msdn.microsoft.com/d22c2c59-0fa1-4452-93f1-dbf151033714">Progressive Decoding Overview</a>
 

 

