---
UID: NF:mfobjects.IMFPluginControl.SetPreferredClsid
title: IMFPluginControl::SetPreferredClsid method
author: windows-driver-content
description: Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.
old-location: mf\imfplugincontrol_imfplugincontrol__setpreferredclsid.htm
old-project: medfound
ms.assetid: c2362150-bb99-43d4-a6e6-7dc240e9826e
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFPluginControl, IMFPluginControl interface [Media Foundation], SetPreferredClsid method, IMFPluginControl::SetPreferredClsid, SetPreferredClsid method [Media Foundation], SetPreferredClsid method [Media Foundation], IMFPluginControl interface, SetPreferredClsid,IMFPluginControl.SetPreferredClsid, mf.imfplugincontrol_imfplugincontrol__setpreferredclsid, mfobjects/IMFPluginControl::SetPreferredClsid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfobjects.h
api_name:
-	IMFPluginControl.SetPreferredClsid
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFPluginControl::SetPreferredClsid method


## -description


Adds a class identifier (CLSID) to the preferred list or removes a CLSID from the list.


## -parameters




### -param pluginType [in]

Member of the <a href="https://msdn.microsoft.com/f967cf3f-582c-457a-ba75-980feb2d9bf3">MF_Plugin_Type</a> enumeration, specifying the type of object.


### -param selector [in]

The key name for the CLSID. For more information about the format of key names, see the Remarks section of <a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a>.


### -param clsid [in]

The CLSID to add to the list. If this parameter is <b>NULL</b>, the key/value entry specified by the <i>selector</i> parameter is removed from the list. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The preferred list is global to the caller's process. Calling this method does not affect the list in other process.




## -see-also




<a href="https://msdn.microsoft.com/cdc6fd4f-c544-43bb-ba99-5468ef49949d">IMFPluginControl</a>
 

 

