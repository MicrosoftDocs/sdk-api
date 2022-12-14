---
UID: NE:mmc.tagIconIdentifier
title: IconIdentifier (mmc.h)
description: The IconIdentifier enumeration is introduced in MMC 1.2.
helpviewer_keywords: ["IconIdentifier","IconIdentifier enumeration [MMC]","Icon_Error","Icon_First","Icon_Information","Icon_Last","Icon_None","Icon_Question","Icon_Warning","_slate_iconidentifier","mmc.iconidentifier","mmc/IconIdentifier","mmc/Icon_Error","mmc/Icon_First","mmc/Icon_Information","mmc/Icon_Last","mmc/Icon_None","mmc/Icon_Question","mmc/Icon_Warning"]
old-location: mmc\iconidentifier.htm
tech.root: mmc
ms.assetid: 5ed7302e-1e2f-46cc-b272-f6c06afe7552
ms.date: 12/05/2018
ms.keywords: IconIdentifier, IconIdentifier enumeration [MMC], Icon_Error, Icon_First, Icon_Information, Icon_Last, Icon_None, Icon_Question, Icon_Warning, _slate_iconidentifier, mmc.iconidentifier, mmc/IconIdentifier, mmc/Icon_Error, mmc/Icon_First, mmc/Icon_Information, mmc/Icon_Last, mmc/Icon_None, mmc/Icon_Question, mmc/Icon_Warning
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: IconIdentifier
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagIconIdentifier
 - mmc/tagIconIdentifier
 - IconIdentifier
 - mmc/IconIdentifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - IconIdentifier
---

# IconIdentifier enumeration


## -description

The 
<b>IconIdentifier</b> enumeration is introduced in MMC 1.2.

The 
<b>IconIdentifier</b> enumeration defines the types of icons that can appear in error messages displayed by the snap-in when 
<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">using the MMC message OCX control</a>.

## -enum-fields

### -field Icon_None:0

No icon displayed in error message.

### -field Icon_Error:32513

Error icon displayed in error message.

### -field Icon_Question:32514

Question icon displayed in error message.

### -field Icon_Warning:32515

Warning icon displayed in error message.

### -field Icon_Information:32516

Information icon displayed in error message.

### -field Icon_First:Icon_Error

Used internally by MMC.

### -field Icon_Last

Used internally by MMC.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-imessageview">IMessageView</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-mmc-message-ocx-control">Using the MMC Message OCX Control</a>
