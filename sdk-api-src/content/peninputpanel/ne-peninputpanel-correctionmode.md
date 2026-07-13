---
UID: NE:peninputpanel.__MIDL___MIDL_itf_peninputpanel_0000_0000_0004
title: CorrectionMode (peninputpanel.h)
description: Specifies the correction modes of the Tablet PC Input Panel.
helpviewer_keywords: ["133d2012-e43c-490a-b126-b7670ea7acf8","CorrectionMode","CorrectionMode enumeration [Tablet PC]","CorrectionMode_NotVisible","CorrectionMode_PostInsertionCollapsed","CorrectionMode_PostInsertionExpanded","CorrectionMode_PreInsertion","peninputpanel/CorrectionMode","peninputpanel/CorrectionMode_NotVisible","peninputpanel/CorrectionMode_PostInsertionCollapsed","peninputpanel/CorrectionMode_PostInsertionExpanded","peninputpanel/CorrectionMode_PreInsertion","tablet.correctionmode"]
old-location: tablet\correctionmode.htm
tech.root: tablet
ms.assetid: 133d2012-e43c-490a-b126-b7670ea7acf8
ms.date: 12/05/2018
ms.keywords: 133d2012-e43c-490a-b126-b7670ea7acf8, CorrectionMode, CorrectionMode enumeration [Tablet PC], CorrectionMode_NotVisible, CorrectionMode_PostInsertionCollapsed, CorrectionMode_PostInsertionExpanded, CorrectionMode_PreInsertion, peninputpanel/CorrectionMode, peninputpanel/CorrectionMode_NotVisible, peninputpanel/CorrectionMode_PostInsertionCollapsed, peninputpanel/CorrectionMode_PostInsertionExpanded, peninputpanel/CorrectionMode_PreInsertion, tablet.correctionmode
req.header: peninputpanel.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CorrectionMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_peninputpanel_0000_0000_0004
 - peninputpanel/__MIDL___MIDL_itf_peninputpanel_0000_0000_0004
 - CorrectionMode
 - peninputpanel/CorrectionMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - peninputpanel.h
api_name:
 - CorrectionMode
---

# CorrectionMode enumeration


## -description

Specifies the correction modes of the Tablet PC Input Panel.

## -enum-fields

### -field CorrectionMode_NotVisible:0

The Input Panel and the correction comb are not visible.

### -field CorrectionMode_PreInsertion:1

The correction comb is shown in pre-insertion mode.

### -field CorrectionMode_PostInsertionCollapsed:2

The correction comb is shown in post-insertion collapsed mode.

### -field CorrectionMode_PostInsertionExpanded:3

The correction comb is shown in post-insertion expanded mode.

## -remarks

When used with the <a href="/windows/desktop/api/peninputpanel/nf-peninputpanel-itextinputpanel-get_currentcorrectionmode">ITextInputPanel::CurrentCorrectionMode Property</a> property it allows an application to determine the current configuration of the Correction Comb.

The <a href="/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel">ITextInputPanel Interface</a> object provides detailed information about and control of the correction mode. Knowing the correction mode helps applications determine the current size of the Input Panel. Controlling how the post-insertion correction expands in an application is one way to customize the correction experience in an application.

There are two basic modes in which the correction comb may appear; pre-insertion and post-insertion. The pre-insertion correction comb corrects text before inserting it into an application. Activate the pre-insertion mode by tapping on the pending text that appears below the baseline in the Writing Pad as the user inks.

The post-insertion correction comb is used to correct text after it has been inserted into an application. Activate the post-insertion mode by placing the insertion point in or selecting text that was previously inserted.

The post-insertion correction comb may appear either above or below Input Panel or it may appear collapsed or expanded. In the collapsed state the post-insertion correction comb only shows a list of alternates. In the expanded state it includes both the alternates and an area to rewrite the word.
