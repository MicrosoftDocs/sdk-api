---
UID: NF:shobjidl.IStartMenuPinnedList.RemoveFromList
title: IStartMenuPinnedList::RemoveFromList (shobjidl.h)
description: Windows Vista:\_Removes an item from the Start menu pinned list, which is the list in the upper left position of the Start menu.
helpviewer_keywords: ["IStartMenuPinnedList interface [Windows Shell]","RemoveFromList method","IStartMenuPinnedList.RemoveFromList","IStartMenuPinnedList::RemoveFromList","RemoveFromList","RemoveFromList method [Windows Shell]","RemoveFromList method [Windows Shell]","IStartMenuPinnedList interface","_shell_IStartMenuPinnedList_RemoveFromList","shell.IStartMenuPinnedList_RemoveFromList","shobjidl/IStartMenuPinnedList::RemoveFromList"]
old-location: shell\IStartMenuPinnedList_RemoveFromList.htm
tech.root: shell
ms.assetid: 8c725c4b-4de6-433b-a647-3c13674084f2
ms.date: 12/05/2018
ms.keywords: IStartMenuPinnedList interface [Windows Shell],RemoveFromList method, IStartMenuPinnedList.RemoveFromList, IStartMenuPinnedList::RemoveFromList, RemoveFromList, RemoveFromList method [Windows Shell], RemoveFromList method [Windows Shell],IStartMenuPinnedList interface, _shell_IStartMenuPinnedList_RemoveFromList, shell.IStartMenuPinnedList_RemoveFromList, shobjidl/IStartMenuPinnedList::RemoveFromList
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
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStartMenuPinnedList::RemoveFromList
 - shobjidl/IStartMenuPinnedList::RemoveFromList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IStartMenuPinnedList.RemoveFromList
---

# IStartMenuPinnedList::RemoveFromList


## -description

<b>Windows Vista</b>: Removes an item from the <b>Start</b> menu pinned list, which is the list in the upper left position of the <b>Start</b> menu.

<b>Windows 7</b>: Removes an item from the <b>Start</b> menu pinned list and unpins the item from the taskbar.

<b>Windows 8</b>: Unpins the item from the taskbar but does not remove the item from the Start screen. Items cannot be programmatically removed from Start; they can only be unpinned by the user or removed as part of a program's uninstallation.

## -parameters

### -param pitem [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a>*</b>

A pointer to an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem">IShellItem</a> object that represents the item to unpin.

## -returns

Type: <b>HRESULT</b>

<ul>
<li>Returns S_OK if the item was successfully removed from the list of pinned items and/or the taskbar.</li>
<li>Returns S_OK if the item was not pinned at all.</li>
<li>Returns a standard error code otherwise.</li>
</ul>

## -remarks

Because an application cannot know if any of its installed shortcuts have been pinned, this method should be called on any application shortcut being removed from the system. This includes shortcuts placed on the desktop during installation and those added to the <b>Start</b> menu's <b>All Programs</b> list.

It is recommended that all applications use this method to clean up their pinned items during their uninstallation process. Unpinning the application shortcut is not required, but it is strongly recommended for reliability.

This method does not remove the original shortcut represented by <i>pitem</i>. It removes its pinned representation from the <b>Start</b> menu and/or taskbar. Once an item has been removed (unpinned) through this method, then the application can delete the original shortcut.

If an item is pinned to both the <b>Start</b> menu and the taskbar, one call to this method removes it from both locations.

<div class="alert"><b>Note</b>  If your application is using the Windows Installer (MSI) framework to perform the uninstallation, you do not need to call this method explicitly; MSI will make the call to unpin the shortcuts for you.</div>
<div> </div>

#### Examples

This example demonstrates the use of <b>IStartMenuPinnedList::RemoveFromList</b>.


```cpp

HRESULT hr = CoInitializeEx(NULL,COINIT_APARTMENTTHREADED);

if (SUCCEEDED(hr))
{
    IShellItem *pitem;
    hr = SHCreateItemFromParsingName(TEXT("Path to the shortcut"), 
                                     NULL, 
                                     IID_PPV_ARGS(&pitem));     

    //
    // Do setup work here to remove the link, including the unpinning
    // of the item.
    //
        
    if (SUCCEEDED(hr))
    {
        IStartMenuPinnedList *pStartMenuPinnedList;
        
        hr = CoCreateInstance(CLSID_StartMenuPin, 
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_PPV_ARGS(&pStartMenuPinnedList));
        
        if (SUCCEEDED(hr))
        {
            hr = pStartMenuPinnedList->RemoveFromList(pitem);
            pStartMenuPinnedList->Release();
        }
        
        pitem->Release();
    }
}

CoUnitialize();
```