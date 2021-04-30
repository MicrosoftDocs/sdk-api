---
UID: NF:mmc.IConsole2.SetStatusText
title: IConsole2::SetStatusText (mmc.h)
description: The IConsole2::SetStatusText method enables the snap-in to change the text in the status bar. Be aware that this is used only by instances of IComponent.
helpviewer_keywords: ["IConsole2 interface [MMC]","SetStatusText method","IConsole2.SetStatusText","IConsole2::SetStatusText","SetStatusText","SetStatusText method [MMC]","SetStatusText method [MMC]","IConsole2 interface","_slate_iconsole2_setstatustext","mmc.iconsole2_setstatustext","mmc/IConsole2::SetStatusText"]
old-location: mmc\iconsole2_setstatustext.htm
tech.root: mmc
ms.assetid: 31c95dcc-8bb8-4a11-9977-d4fa2ca30992
ms.date: 12/05/2018
ms.keywords: IConsole2 interface [MMC],SetStatusText method, IConsole2.SetStatusText, IConsole2::SetStatusText, SetStatusText, SetStatusText method [MMC], SetStatusText method [MMC],IConsole2 interface, _slate_iconsole2_setstatustext, mmc.iconsole2_setstatustext, mmc/IConsole2::SetStatusText
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IConsole2::SetStatusText
 - mmc/IConsole2::SetStatusText
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IConsole2.SetStatusText
---

# IConsole2::SetStatusText


## -description

The <b>IConsole2::SetStatusText</b> method enables the snap-in to change the text in the status bar. Be aware that this is used only by instances of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>.

## -parameters

### -param pszStatusText [in]

A pointer to a null-terminated string that contains text to be displayed in the status bar.

## -returns

This method can return one of these values.

## -remarks

The status bar has three sections, which are delineated by the pipe character (|). For example, setting the text in the status bar to "Left| Middle| Right" places "Left" in the leftmost section of the status bar, " Middle" in the middle section, and " Right" in the rightmost section.

If more than three fields are delineated (that is, there are more than two pipes), then everything that would be placed in the fourth and higher fields is omitted.

In addition, the middle section is designed to function as a progress bar. This functionality is invoked by passing the '%' character as the first character, followed by a number between 0 and 100, into the middle section. Instead of text, this section then displays a progress bar that is zero to 100 percent complete. For example, passing "Done|%75" places "Done" in the left section and a progress bar 75% complete in the middle section.

To display a string that begins with '%' in the middle section of the status bar, then begin the string with '%%'. This causes the middle section to display text and removes the first '%'. For example: "Today is|%%Wednesday%" results in the left section that contains "Today is" and the middle section that contains "%Wednesday%". If an invalid number or non-numeric text is entered in the middle section following a '%', then the middle section is empty. If a '%' is the only character in the section, then it will be shown as text.

This method should be called from an 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a> interface pointer obtained through 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>.

Only the snap-in that owns the currently selected scope item can change the status bar text.

In MMC version 1.1 and later, each multiple-document interface (MDI) child window has a status bar.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>