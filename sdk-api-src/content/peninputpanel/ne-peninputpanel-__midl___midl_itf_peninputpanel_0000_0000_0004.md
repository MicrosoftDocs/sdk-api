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

# __MIDL___MIDL_itf_peninputpanel_0000_0000_0004 enumeration


## -description



Specifies the correction modes of the Tablet PC Input Panel.




## -enum-fields




### -field CorrectionMode_NotVisible

The Input Panel and the correction comb are not visible.


### -field CorrectionMode_PreInsertion

The correction comb is shown in pre-insertion mode.


### -field CorrectionMode_PostInsertionCollapsed

The correction comb is shown in post-insertion collapsed mode.


### -field CorrectionMode_PostInsertionExpanded

The correction comb is shown in post-insertion expanded mode.


## -remarks



When used with the <a href="https://msdn.microsoft.com/92cd44a0-4dc6-4882-9ebb-45aa5b3fbc69">ITextInputPanel::CurrentCorrectionMode Property</a> property it allows an application to determine the current configuration of the Correction Comb.

The <a href="https://msdn.microsoft.com/1e719900-db58-430d-9059-efb3f884f6f0">ITextInputPanel Interface</a> object provides detailed information about and control of the correction mode. Knowing the correction mode helps applications determine the current size of the Input Panel. Controlling how the post-insertion correction expands in an application is one way to customize the correction experience in an application.

There are two basic modes in which the correction comb may appear; pre-insertion and post-insertion. The pre-insertion correction comb corrects text before inserting it into an application. Activate the pre-insertion mode by tapping on the pending text that appears below the baseline in the Writing Pad as the user inks.

The post-insertion correction comb is used to correct text after it has been inserted into an application. Activate the post-insertion mode by placing the insertion point in or selecting text that was previously inserted.

The post-insertion correction comb may appear either above or below Input Panel or it may appear collapsed or expanded. In the collapsed state the post-insertion correction comb only shows a list of alternates. In the expanded state it includes both the alternates and an area to rewrite the word.



