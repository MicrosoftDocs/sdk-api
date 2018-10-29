---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.GetOsProductContentId
title: IEditionUpgradeHelper::GetOsProductContentId
author: windows-sdk-content
description: Retrieves the content identifier that corresponds to the current installation of the operating system. The content identifier is used to look up the operating system product in the store catalog.
old-location: winprog\ieditionupgradehelper_getosproductcontentid.htm
tech.root: DevNotes
ms.assetid: 79EEDFF2-FDF9-4BC9-968A-3543892AE870
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: GetOsProductContentId, GetOsProductContentId method [Windows API], GetOsProductContentId method [Windows API],IEditionUpgradeHelper interface, IEditionUpgradeHelper interface [Windows API],GetOsProductContentId method, IEditionUpgradeHelper.GetOsProductContentId, IEditionUpgradeHelper::GetOsProductContentId, editionupgradehelper/IEditionUpgradeHelper::GetOsProductContentId, winprog.ieditionupgradehelper_getosproductcontentid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: editionupgradehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Editionupgradehelper.idl
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
 - editionupgradehelper.h
api_name:
 - IEditionUpgradeHelper.GetOsProductContentId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEditionUpgradeHelper::GetOsProductContentId


## -description


Retrieves the content identifier that corresponds to the current installation of the operating system. The content identifier is used to look up the operating system product in the store catalog.


## -parameters




### -param contentId [out]

The content identifier that corresponds to the current installation of the operating system.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2A243B2F-F7A1-448F-B16D-143514725658">IEditionUpgradeHelper</a>



<a href="https://msdn.microsoft.com/C7A97C7E-654D-4717-975F-41B05F3BE901">UpdateOperatingSystem</a>
 

 

