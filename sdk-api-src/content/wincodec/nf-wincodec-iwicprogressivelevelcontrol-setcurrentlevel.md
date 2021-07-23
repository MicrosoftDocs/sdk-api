---
UID: NF:wincodec.IWICProgressiveLevelControl.SetCurrentLevel
title: IWICProgressiveLevelControl::SetCurrentLevel (wincodec.h)
description: Specifies the level to retrieve on the next call to CopyPixels.
helpviewer_keywords: ["IWICProgressiveLevelControl interface [Windows Imaging Component]","SetCurrentLevel method","IWICProgressiveLevelControl.SetCurrentLevel","IWICProgressiveLevelControl::SetCurrentLevel","SetCurrentLevel","SetCurrentLevel method [Windows Imaging Component]","SetCurrentLevel method [Windows Imaging Component]","IWICProgressiveLevelControl interface","_wic_codec_iwicprogressivelevelcontrol_setcurrentlevel","wic._wic_codec_iwicprogressivelevelcontrol_setcurrentlevel","wincodec/IWICProgressiveLevelControl::SetCurrentLevel"]
old-location: wic\_wic_codec_iwicprogressivelevelcontrol_setcurrentlevel.htm
tech.root: wic
ms.assetid: b4a2c279-385d-4177-bd8f-a49f545c692a
ms.date: 12/05/2018
ms.keywords: IWICProgressiveLevelControl interface [Windows Imaging Component],SetCurrentLevel method, IWICProgressiveLevelControl.SetCurrentLevel, IWICProgressiveLevelControl::SetCurrentLevel, SetCurrentLevel, SetCurrentLevel method [Windows Imaging Component], SetCurrentLevel method [Windows Imaging Component],IWICProgressiveLevelControl interface, _wic_codec_iwicprogressivelevelcontrol_setcurrentlevel, wic._wic_codec_iwicprogressivelevelcontrol_setcurrentlevel, wincodec/IWICProgressiveLevelControl::SetCurrentLevel
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
 - IWICProgressiveLevelControl::SetCurrentLevel
 - wincodec/IWICProgressiveLevelControl::SetCurrentLevel
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
 - IWICProgressiveLevelControl.SetCurrentLevel
---

# IWICProgressiveLevelControl::SetCurrentLevel


## -description

Specifies the level to retrieve on the next call to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a>.

## -parameters

### -param nLevel [in]

Type: <b>UINT</b>

Specifies which level to return next. If greater than the total number of levels supported, an error will be returned.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A call does not have to request every level supported.
        If a caller requests level 1, without having previously requested level 0, the bits returned by the next call to <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapsource-copypixels">CopyPixels</a> will include both levels.
      

If the requested level is invalid, the error returned is <a href="/windows/desktop/wic/-wic-codec-error-codes">WINCODEC_ERR_INVALIDPROGRESSIVELEVEL</a>.


#### Examples

Users should use this method to iterate through the progressive levels of a progressive JPEG image rather than the <a href="/windows/desktop/api/wincodec/nf-wincodec-iwicprogressivelevelcontrol-getcurrentlevel">GetCurrentLevel</a> method. JPEG progressive levels are determined by the image and do not have a fixed level count. 
         Using <b>GetCurrentLevel</b> method will force the application to wait for all progressive levels to be downloaded before it can return. 
         Instead, applications should use the following code to iterate through the progressive levels of a progressive JPEG image.


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