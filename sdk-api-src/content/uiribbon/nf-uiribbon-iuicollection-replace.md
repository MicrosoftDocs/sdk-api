---
UID: NF:uiribbon.IUICollection.Replace
title: IUICollection::Replace
author: windows-sdk-content
description: Replaces an item at the specified index of the IUICollection with another item.
old-location: windowsribbon\windowsribbon_iuicollection_replace.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollection\replace.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUICollection interface [Windows Ribbon],Replace method, IUICollection.Replace, IUICollection::Replace, Replace, Replace method [Windows Ribbon], Replace method [Windows Ribbon],IUICollection interface, scenicintent_IUICollection_Replace, uiribbon/IUICollection::Replace, windowsribbon.windowsribbon_iuicollection_replace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mshtml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUICollection.Replace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiribbon.h
: 
- IUICollection.Replace
: 
req.product: Windows UI
---

# IUICollection::Replace


## -description


Replaces an item at the specified index of the <a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a> with another item.


## -parameters




### -param indexReplaced [in]

Type: <b>UINT32</b>

The zero-based index of <i>item</i> to be replaced in the <a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a>.
				


### -param itemReplaceWith [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>*</b>

Pointer to the replacement item that is added to the <a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd742704(v=VS.85).aspx">Gallery Sample</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a>
 

 

