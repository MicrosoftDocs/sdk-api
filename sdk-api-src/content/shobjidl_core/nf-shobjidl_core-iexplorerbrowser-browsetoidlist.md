---
UID: NF:shobjidl_core.IExplorerBrowser.BrowseToIDList
title: IExplorerBrowser::BrowseToIDList
author: windows-sdk-content
description: Browses to a pointer to an item identifier list (PIDL)
old-location: shell\IExplorerBrowser_BrowseToIDList.htm
tech.root: shell
ms.assetid: b0633072-e059-4ea4-b9c0-798399ccf66a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: BrowseToIDList, BrowseToIDList method [Windows Shell], BrowseToIDList method [Windows Shell],IExplorerBrowser interface, IExplorerBrowser interface [Windows Shell],BrowseToIDList method, IExplorerBrowser.BrowseToIDList, IExplorerBrowser::BrowseToIDList, SBSP_ABSOLUTE, SBSP_KEEPWORDWHEELTEXT, SBSP_NAVIGATEBACK, SBSP_NAVIGATEFORWARD, SBSP_PARENT, SBSP_RELATIVE, _shell_IExplorerBrowser_BrowseToIDList, shell.IExplorerBrowser_BrowseToIDList, shobjidl_core/IExplorerBrowser::BrowseToIDList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - IExplorerBrowser.BrowseToIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExplorerBrowser::BrowseToIDList


## -description


Browses to a pointer to an item identifier list (PIDL)


## -parameters




### -param pidl [in]

Type: <b>PCUIDLIST_RELATIVE</b>

A pointer to a const <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> (item identifier list) that specifies an object's location as the destination to navigate to. This parameter can be <b>NULL</b>. For more information, see Remarks.


### -param uFlags [in]

Type: <b>UINT</b>

A flag that specifies the category of the <i>pidl</i>. This affects how navigation is accomplished. Must be the value zero, or a bitwise combination of the following values.



#### SBSP_ABSOLUTE

An absolute PIDL, relative to the desktop.



#### SBSP_RELATIVE

A relative PIDL, relative to the current folder.



#### SBSP_PARENT

Browse to the parent folder, ignore the PIDL.



#### SBSP_NAVIGATEBACK

Navigate back, ignore the PIDL.



#### SBSP_NAVIGATEFORWARD

Navigate forward, ignore the PIDL.





#### SBSP_KEEPWORDWHEELTEXT

<b>Windows Vista and later</b>. This flag indicates that any search text entered by a WordWheel (the Search box in Windows Explorer) should be preserved during this navigation, so that items at the new location are filtered in the same way they were filtered at the previous location.




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The parameter <i>pidl</i> may be <b>NULL</b> if the flags specified in <i>uFlags</i> indicate navigation through the built-in TravelLog, that is, SBSP_NAVIGATEBACK or SBSP_NAVIGATEFORWARD.

 This method supports only a subset of the SBSP flags listed in the shobjidl.h file. Consequently, this method returns E_INVALIDARG if SBSP_NEWBROWSER or SBSP_EXPLOREMODE are specified in <i>uFlags</i>.




## -see-also




<a href="https://msdn.microsoft.com/e391ca11-25e3-4d97-8efd-0afd74a3e5c2">BrowseObject</a>



<a href="https://msdn.microsoft.com/da2cf5d4-5a68-4d18-807b-b9d4e2712c10">IExplorerBrowser</a>
 

 

