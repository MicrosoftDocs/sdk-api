---
UID: NF:mfobjects.IMFPluginControl.SetPreferredClsid
title: IMFPluginControl::SetPreferredClsid (mfobjects.h)
author: windows-sdk-content
description: Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.
old-location: mf\imfplugincontrol_imfplugincontrol__setpreferredclsid.htm
tech.root: medfound
ms.assetid: c2362150-bb99-43d4-a6e6-7dc240e9826e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFPluginControl interface [Media Foundation],SetPreferredClsid method, IMFPluginControl.SetPreferredClsid, IMFPluginControl::SetPreferredClsid, SetPreferredClsid, SetPreferredClsid method [Media Foundation], SetPreferredClsid method [Media Foundation],IMFPluginControl interface, mf.imfplugincontrol_imfplugincontrol__setpreferredclsid, mfobjects/IMFPluginControl::SetPreferredClsid
ms.topic: method
f1_keywords: ["mfobjects/IMFPluginControl.SetPreferredClsid"]
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - mfobjects.h
api_name:
 - IMFPluginControl.SetPreferredClsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPluginControl::SetPreferredClsid


## -description


Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.


## -parameters




### -param pluginType [in]

Member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ne-mfobjects-_mf_plugin_type">MF_Plugin_Type</a> enumeration, specifying the type of object.


### -param selector [in]

The key name for the CLSID. For more information about the format of key names, see the Remarks section of <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>.


### -param clsid [in]

The CLSID to add to the list. If this parameter is <b>NULL</b>, the key/value entry specified by the <i>selector</i> parameter is removed from the list. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The preferred list is global to the caller's process. Calling this method does not affect the list in other process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfplugincontrol">IMFPluginControl</a>
 

 

