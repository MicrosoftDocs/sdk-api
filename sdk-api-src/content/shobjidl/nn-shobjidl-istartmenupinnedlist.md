---
UID: NN:shobjidl.IStartMenuPinnedList
title: IStartMenuPinnedList
author: windows-sdk-content
description: Exposes a method that unpins an application shortcut from the Start menu or the taskbar.
old-location: shell\IStartMenuPinnedList.htm
tech.root: shell
ms.assetid: e1f4dbdb-34c0-4bf5-bb8b-a622a81c1617
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: IStartMenuPinnedList, IStartMenuPinnedList interface [Windows Shell], IStartMenuPinnedList interface [Windows Shell],described, _shell_IStartMenuPinnedList, shell.IStartMenuPinnedList, shobjidl/IStartMenuPinnedList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll (version 6.0.6000 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IStartMenuPinnedList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStartMenuPinnedList interface


## -description


Exposes a method that unpins an application shortcut from the <b>Start</b> menu or the taskbar.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStartMenuPinnedList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IStartMenuPinnedList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IStartMenuPinnedList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c725c4b-4de6-433b-a647-3c13674084f2">RemoveFromList</a>
</td>
<td align="left" width="63%">
<b>Windows Vista</b>: Removes an item from the <b>Start</b> menu pinned list, which is the list in the upper left position of the <b>Start</b> menu.

<b>Windows 7</b>: Removes an item from the <b>Start</b> menu pinned list and unpins the item from the taskbar.

<b>Windows 8</b>: Unpins the item from the taskbar but does not remove the item from the Start screen.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Windows provides an implementation of this interface as CLSID_StartMenuPin. Third parties do not provide their own implementation.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Any shortcut installed by an application might have been subsequently pinned by the user, and there is no way for an application to know this. Therefore, we recommend that, during uninstallation, all applications call <a href="https://msdn.microsoft.com/8c725c4b-4de6-433b-a647-3c13674084f2">IStartMenuPinnedList::RemoveFromList</a> on each shortcut they installed.



Note that <b>IStartMenuPinnedList</b> does not remove the shortcuts themselves, it only unpins them. Applications first call <a href="https://msdn.microsoft.com/8c725c4b-4de6-433b-a647-3c13674084f2">IStartMenuPinnedList::RemoveFromList</a> on a shortcut, then delete that shortcut.

<h3><a id="Compatibility"></a><a id="compatibility"></a><a id="COMPATIBILITY"></a>Compatibility</h3>
In Windows 8, the Start screen replaces the legacy Start menu. CLSID_StartMenuPin and <b>IStartMenuPinnedList</b> are present in Windows 8 to provide backward compatibility with existing applications, but they do not affect <a href="https://msdn.microsoft.com/3F837E35-6134-417c-899F-E09CD40085E8">tiles</a> pinned to the Windows 8 Start screen. CLSID_StartMenuPin and <b>IStartMenuPinnedList</b> do continue to impact items pinned to the Windows 8 desktop taskbar.



