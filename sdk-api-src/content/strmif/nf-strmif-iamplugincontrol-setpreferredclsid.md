---
UID: NF:strmif.IAMPluginControl.SetPreferredClsid
title: IAMPluginControl::SetPreferredClsid (strmif.h)
author: windows-sdk-content
description: Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.
old-location: dshow\iamplugincontrol_setpreferredclsid.htm
tech.root: DirectShow
ms.assetid: 45702714-6b35-4863-885e-55049258a4ae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMPluginControl interface [DirectShow],SetPreferredClsid method, IAMPluginControl.SetPreferredClsid, IAMPluginControl::SetPreferredClsid, SetPreferredClsid, SetPreferredClsid method [DirectShow], SetPreferredClsid method [DirectShow],IAMPluginControl interface, dshow.iamplugincontrol_setpreferredclsid, strmif/IAMPluginControl::SetPreferredClsid
ms.topic: method
f1_keywords: 
 - "strmif/IAMPluginControl.SetPreferredClsid"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Axextend.idl
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
 - Strmif.h
api_name:
 - IAMPluginControl.SetPreferredClsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMPluginControl::SetPreferredClsid


## -description


Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.


## -parameters




### -param subType [in]

A media subtype GUID to associate with the CLSID.


### -param clsid [in]

Pointer to the CLSID to add to the list. If this parameter is <b>NULL</b>, the entry associated with <i>subType</i> is removed from the list


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamplugincontrol">IAMPluginControl</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/intelligent-connect">Intelligent Connect</a>
 

 

