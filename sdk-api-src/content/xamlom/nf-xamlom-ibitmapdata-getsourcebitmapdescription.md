---
UID: NF:xamlom.IBitmapData.GetSourceBitmapDescription
title: IBitmapData::GetSourceBitmapDescription
author: windows-sdk-content
description: Gets a BitmapDescription that describes the original format of the bitmap data stored in the IBitmapData.
old-location: xaml_diagnostics\ibitmapdata_getsourcebitmapdescription.htm
tech.root: xaml_diagnostics
ms.assetid: 3B11A54C-347D-4F14-A5F8-36250FC5E06B
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSourceBitmapDescription, GetSourceBitmapDescription method, GetSourceBitmapDescription method,IBitmapData interface, IBitmapData interface,GetSourceBitmapDescription method, IBitmapData.GetSourceBitmapDescription, IBitmapData::GetSourceBitmapDescription, xaml_diagnostics.ibitmapdata_getsourcebitmapdescription, xamlom/IBitmapData::GetSourceBitmapDescription
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBitmapData::GetSourceBitmapDescription


## -description


Gets a <a href="https://msdn.microsoft.com/C5E1BA37-738C-4251-8648-681C58B740E1">BitmapDescription</a> that describes the original format of the bitmap data stored in the <a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>.


## -parameters




### -param pBitmapDescription [out]

Information about the original format of the  bitmap stored in the <a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This will have the same value as the <a href="https://msdn.microsoft.com/C5E1BA37-738C-4251-8648-681C58B740E1">BitmapDescription</a> returned by <a href="https://msdn.microsoft.com/B10BF4E3-C9C2-41E6-99FC-671F6BE47278">GetBitmapDescription</a> unless the bitmap data was format converted or scaled. Format conversion and scaling will occur as necessary to meet the contract of the method that returned the <a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>. 




## -see-also




<a href="https://msdn.microsoft.com/5B833E2A-D150-4ECA-88C8-CEEDBF2E23C6">IBitmapData</a>
 

 

