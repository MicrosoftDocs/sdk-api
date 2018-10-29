---
UID: NF:fhcfg.IFhConfigMgr.ChangeDefaultTargetRecommendation
title: IFhConfigMgr::ChangeDefaultTargetRecommendation
author: windows-sdk-content
description: Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.
old-location: winprog\ifhconfigmgr_changedefaulttargetrecommendation.htm
tech.root: DevNotes
ms.assetid: 40F22464-FE28-40A0-85C6-74C5BD819E83
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: ChangeDefaultTargetRecommendation, ChangeDefaultTargetRecommendation method [Windows API], ChangeDefaultTargetRecommendation method [Windows API],FhConfigMgr class, ChangeDefaultTargetRecommendation method [Windows API],IFhConfigMgr interface, FhConfigMgr class [Windows API],ChangeDefaultTargetRecommendation method, IFhConfigMgr interface [Windows API],ChangeDefaultTargetRecommendation method, IFhConfigMgr.ChangeDefaultTargetRecommendation, IFhConfigMgr::ChangeDefaultTargetRecommendation, fhcfg/IFhConfigMgr::ChangeDefaultTargetRecommendation, winprog.ifhconfigmgr_changedefaulttargetrecommendation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - Fhcfg.h
api_name:
 - IFhConfigMgr.ChangeDefaultTargetRecommendation
 - FhConfigMgr.ChangeDefaultTargetRecommendation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFhConfigMgr::ChangeDefaultTargetRecommendation


## -description


Causes the currently assigned backup target to be recommended or not recommended to other members of the home group that the computer belongs to.


## -parameters




### -param Recommend [in]

If set to <b>TRUE</b>, the currently assigned backup target is recommended to other members of the home group. If set to <b>FALSE</b> and the currently assigned backup target is currently recommended to other members of the home group, this recommendation is withdrawn.



## -returns



If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code such as one of the values defined in the FhErrors.h header file.




## -remarks



When a backup target is recommended to other computers in the home group, users on those computers see that storage device in the list of available backup targets in the File History item in Control Panel. 

If the backup target is not recommended to other computers in the home group, or if the recommendation is withdrawn, the target does not appear in the list of available backup targets on the other computers.

A backup target cannot be recommended or not recommended on a computer that is joined to a domain or on a computer that is having ARM architecture.




## -see-also




<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>
 

 

