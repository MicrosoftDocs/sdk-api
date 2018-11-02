---
UID: NF:imepad.IImeSpecifyApplets.GetAppletIIDList
title: IImeSpecifyApplets::GetAppletIIDList
author: windows-sdk-content
description: Called from the IImePad interface to enumerate the IImePadApplet interfaces that are implemented.
old-location: intl\iimespecifyapplets_getappletiidlist.htm
tech.root: Intl
ms.assetid: 05FD7E9A-5C65-4FB7-B509-591B4B434961
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetAppletIIDList, GetAppletIIDList method [Internationalization for Windows Applications], GetAppletIIDList method [Internationalization for Windows Applications],IImeSpecifyApplets interface, IImeSpecifyApplets interface [Internationalization for Windows Applications],GetAppletIIDList method, IImeSpecifyApplets.GetAppletIIDList, IImeSpecifyApplets::GetAppletIIDList, imepad/IImeSpecifyApplets::GetAppletIIDList, intl.iimespecifyapplets_getappletiidlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imepad.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Imepad.h
api_name:
 - IImeSpecifyApplets.GetAppletIIDList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IImeSpecifyApplets::GetAppletIIDList


## -description


Called from the <a href="https://msdn.microsoft.com/6604112A-5BD5-4B2C-AECC-D09180B04D7F">IImePad</a> interface to enumerate the <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a> interfaces that are implemented.


## -parameters




### -param refiid [in]

IID of the <a href="https://msdn.microsoft.com/F3BC7176-9659-47B6-AFCA-049807394961">IImePadApplet</a> interface. This IID is defined in Imepad.h as <b>IID_IImePadApplet</b>. This is for <b>IImePadApplet</b>'s future enhancement


### -param lpIIDList [in, out]

Pointer to a APPLETIIDLIST structure. Sets the applet's IID list and count.


## -returns



<b>S_OK</b> if successful, otherwise <b>E_FAIL</b>.




## -see-also




<a href="https://msdn.microsoft.com/788C7272-3BFF-4531-B66E-211585BF85E3">IImeSpecifyApplets</a>
 

 

