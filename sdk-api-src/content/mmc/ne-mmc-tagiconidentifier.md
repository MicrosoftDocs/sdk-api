---
UID: NE:mmc.tagIconIdentifier
title: tagIconIdentifier
author: windows-sdk-content
description: The IconIdentifier enumeration is introduced in MMC 1.2.
old-location: mmc\iconidentifier.htm
old-project: mmc
ms.assetid: 5ed7302e-1e2f-46cc-b272-f6c06afe7552
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: IconIdentifier, IconIdentifier enumeration [MMC], Icon_Error, Icon_First, Icon_Information, Icon_Last, Icon_None, Icon_Question, Icon_Warning, _slate_iconidentifier, mmc.iconidentifier, mmc/IconIdentifier, mmc/Icon_Error, mmc/Icon_First, mmc/Icon_Information, mmc/Icon_Last, mmc/Icon_None, mmc/Icon_Question, mmc/Icon_Warning, tagIconIdentifier
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: IconIdentifier
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - IconIdentifier
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# tagIconIdentifier enumeration


## -description


The 
<b>IconIdentifier</b> enumeration is introduced in MMC 1.2.

The 
<b>IconIdentifier</b> enumeration defines the types of icons that can appear in error messages displayed by the snap-in when 
<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">using the MMC message OCX control</a>.


## -enum-fields




### -field Icon_None

No icon displayed in error message.


### -field Icon_Error

Error icon displayed in error message.


### -field Icon_Question

Question icon displayed in error message.


### -field Icon_Warning

Warning icon displayed in error message.


### -field Icon_Information

Information icon displayed in error message.


### -field Icon_First

Used internally by MMC.


### -field Icon_Last

Used internally by MMC.


## -see-also




<a href="https://msdn.microsoft.com/e1ea6bb2-f35e-4379-b4e4-70d4e5d77b93">IMessageView</a>



<a href="https://msdn.microsoft.com/bc6db308-d8dd-4868-803d-45c64b951192">Using the MMC Message OCX Control</a>
 

 

