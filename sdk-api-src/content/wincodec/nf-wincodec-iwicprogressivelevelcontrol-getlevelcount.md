---
UID: NF:wincodec.IWICProgressiveLevelControl.GetLevelCount
title: IWICProgressiveLevelControl::GetLevelCount (wincodec.h)
description: Gets the number of levels of progressive decoding supported by the CODEC.
helpviewer_keywords: ["GetLevelCount","GetLevelCount method [Windows Imaging Component]","GetLevelCount method [Windows Imaging Component]","IWICProgressiveLevelControl interface","IWICProgressiveLevelControl interface [Windows Imaging Component]","GetLevelCount method","IWICProgressiveLevelControl.GetLevelCount","IWICProgressiveLevelControl::GetLevelCount","_wic_codec_iwicprogressivelevelcontrol_getlevelcount","wic._wic_codec_iwicprogressivelevelcontrol_getlevelcount","wincodec/IWICProgressiveLevelControl::GetLevelCount"]
old-location: wic\_wic_codec_iwicprogressivelevelcontrol_getlevelcount.htm
tech.root: wic
ms.assetid: f7949d31-c679-43ea-aa07-5f9f8579b4f7
ms.date: 12/05/2018
ms.keywords: GetLevelCount, GetLevelCount method [Windows Imaging Component], GetLevelCount method [Windows Imaging Component],IWICProgressiveLevelControl interface, IWICProgressiveLevelControl interface [Windows Imaging Component],GetLevelCount method, IWICProgressiveLevelControl.GetLevelCount, IWICProgressiveLevelControl::GetLevelCount, _wic_codec_iwicprogressivelevelcontrol_getlevelcount, wic._wic_codec_iwicprogressivelevelcontrol_getlevelcount, wincodec/IWICProgressiveLevelControl::GetLevelCount
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWICProgressiveLevelControl::GetLevelCount
 - wincodec/IWICProgressiveLevelControl::GetLevelCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Windowscodecs.dll
api_name:
 - IWICProgressiveLevelControl.GetLevelCount
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Users should not use this function to iterate through the progressive levels of a progressive JPEG image. JPEG progressive levels are determined by the image and do not have a fixed level count. Using this method will force the application to wait for all progressive levels to be downloaded before it can return. Instead, applications should use the following code to iterate through the progressive levels of a progressive JPEG image.


#### Examples


```
IWICProgressiveLevelControl *pProgressive = NULL;

HRESULT hr = (pBitmapFrame->QueryInterface(
   IID_IWICProgressiveLevelControl, 
   (void**) &pProgressive));
                
if (SUCCEEDED(hr))
{
   for (UINT uCurrentLevel = 0; SUCCEEDED(hr); uCurrentLevel++)
   {
      hr = pProgressive->SetCurrentLevel(uCurrentLevel);
      if (WINCODEC_ERR_INVALIDPROGRESSIVELEVEL == hr)
      {
         // No more levels
         break;
      }

      if (SUCCEEDED(hr))
      {
         // Output the current level
         hr = pBitmapFrame->CopyPixels(...);
      }                      
   }
}

if (pProgressive)
{
   pProgressive->Release();
}
```

## -see-also

<a href="/windows/desktop/api/wincodec/nn-wincodec-iwicprogressivelevelcontrol">IWICProgressiveLevelControl</a>



<a href="/windows/desktop/wic/-wic-progressive-decoding">Progressive Decoding Overview</a>