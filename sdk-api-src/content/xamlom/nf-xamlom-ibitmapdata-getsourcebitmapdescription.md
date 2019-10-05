---
UID: NF:xamlom.IBitmapData.GetSourceBitmapDescription
title: IBitmapData::GetSourceBitmapDescription (xamlom.h)
author: windows-sdk-content
description: Gets a BitmapDescription that describes the original format of the bitmap data stored in the IBitmapData.
old-location: xaml_diagnostics\ibitmapdata_getsourcebitmapdescription.htm
tech.root: xaml_diagnostics
ms.assetid: 3B11A54C-347D-4F14-A5F8-36250FC5E06B
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetSourceBitmapDescription, GetSourceBitmapDescription method, GetSourceBitmapDescription method,IBitmapData interface, IBitmapData interface,GetSourceBitmapDescription method, IBitmapData.GetSourceBitmapDescription, IBitmapData::GetSourceBitmapDescription, xaml_diagnostics.ibitmapdata_getsourcebitmapdescription, xamlom/IBitmapData::GetSourceBitmapDescription
ms.topic: method
f1_keywords: 
 - "xamlom/IBitmapData.GetSourceBitmapDescription"
dev_langs:
 - c++
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IBitmapData.GetSourceBitmapDescription
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IBitmapData::GetSourceBitmapDescription


## -description


Gets a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/ns-xamlom-bitmapdescription">BitmapDescription</a> that describes the original format of the bitmap data stored in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>.


## -parameters




### -param pBitmapDescription [out]

Information about the original format of the  bitmap stored in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This will have the same value as the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/ns-xamlom-bitmapdescription">BitmapDescription</a> returned by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ibitmapdata-getbitmapdescription">GetBitmapDescription</a> unless the bitmap data was format converted or scaled. Format conversion and scaling will occur as necessary to meet the contract of the method that returned the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ibitmapdata">IBitmapData</a>
 

 

