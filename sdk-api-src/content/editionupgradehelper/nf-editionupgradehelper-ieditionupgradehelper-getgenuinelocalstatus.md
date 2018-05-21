---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.GetGenuineLocalStatus
title: IEditionUpgradeHelper::GetGenuineLocalStatus
author: windows-driver-content
description: Retrieves whether the currently installed operating system is activated.
old-location: winprog\ieditionupgradehelper_getgenuinelocalstatus.htm
old-project: DevNotes
ms.assetid: 061AECF0-AC7A-480F-B532-F5D8AC078168
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: GetGenuineLocalStatus, GetGenuineLocalStatus method [Windows API], GetGenuineLocalStatus method [Windows API],IEditionUpgradeHelper interface, IEditionUpgradeHelper interface [Windows API],GetGenuineLocalStatus method, IEditionUpgradeHelper.GetGenuineLocalStatus, IEditionUpgradeHelper::GetGenuineLocalStatus, editionupgradehelper/IEditionUpgradeHelper::GetGenuineLocalStatus, winprog.ieditionupgradehelper_getgenuinelocalstatus
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
req.typenames: EAP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	editionupgradehelper.h
api_name:
-	IEditionUpgradeHelper.GetGenuineLocalStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEditionUpgradeHelper::GetGenuineLocalStatus


## -description


Retrieves whether the currently installed operating system is activated.


## -parameters




### -param isGenuine [out]

TRUE is the currently installed operating system is activated; otherwise, FALSE.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2A243B2F-F7A1-448F-B16D-143514725658">IEditionUpgradeHelper</a>
 

 

