---
UID: NF:shobjidl_core.ICustomDestinationList.DeleteList
title: ICustomDestinationList::DeleteList
author: windows-sdk-content
description: Deletes a custom Jump List for a specified application.
old-location: shell\ICustomDestinationList_DeleteList.htm
tech.root: shell
ms.assetid: ef246f5a-9fcf-4475-b19a-e676f0351f3f
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: DeleteList, DeleteList method [Windows Shell], DeleteList method [Windows Shell],ICustomDestinationList interface, ICustomDestinationList interface [Windows Shell],DeleteList method, ICustomDestinationList.DeleteList, ICustomDestinationList::DeleteList, _shell_ICustomDestinationList_DeleteList, shell.ICustomDestinationList_DeleteList, shobjidl_core/ICustomDestinationList::DeleteList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.1 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - ICustomDestinationList.DeleteList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICustomDestinationList::DeleteList


## -description


Deletes a custom Jump List for a specified application.


## -parameters




### -param pszAppID [in]

Type: <b>LPCWSTR</b>

A pointer to the AppUserModelID of the process whose taskbar button representation displays the custom Jump List. In the beta release of Windows 7, this AppUserModelID must be explicitly provided because this method is intended to be called from an uninstaller, which runs in a separate process. Because it is in a separate process, the system cannot reliably deduce the AppUserModelID. This restriction is expected to be removed in later releases.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



There are several instances where this method should be called, including:
            
                

<ul>
<li>When the application is uninstalled.</li>
<li>When the user clears history from within the application.</li>
<li>When the user disables destination tracking in the application's Settings or Options pages.</li>
</ul>
This method should not be called when an application is updating a custom destination list. It is used only to completely clear the list during an uninstall operation, or if the application provides an option for the user to turn off the list.

After the custom Jump List has been removed, a standard Jump List generated from system-generated data for recently used items is shown. If no such data has been collected or if the information has been cleared through <a href="https://msdn.microsoft.com/bda83a9a-9759-47cc-8d15-ac55583a5810">RemoveAllDestinations</a>, the Jump List might contain only its minimum, always present content: standard tasks to pin or unpin, launch a new instance of the application, or close windows.




## -see-also




<a href="https://msdn.microsoft.com/ebce2d99-6f20-4545-9f12-d79cd8d0828f">Application User Model IDs (AppUserModelIDs)</a>



<a href="https://msdn.microsoft.com/65a3dab8-3136-416d-bd8a-ca813bfe0533">ICustomDestinationList</a>



<a href="https://msdn.microsoft.com/7b3a5d32-bf44-4c4f-9b31-6c0a82aac6fd">ICustomDestinationList::SetAppID</a>



<a href="https://msdn.microsoft.com/cbf2b07d-d67c-4755-888c-d40692d13cae">Taskbar Extensions</a>
 

 

