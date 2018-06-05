---
UID: NF:richole.IRichEditOle.ConvertObject
title: IRichEditOle::ConvertObject
author: windows-sdk-content
description: Converts an object to a new type. This call reloads the object but does not force an update; the caller must do this.
old-location: controls\IRichEditOle_ConvertObject.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\richedit\richeditcontrols\richeditcontrolreference\richeditinterfaces\iricheditole\iricheditoleconvertobject.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: ConvertObject, ConvertObject method [Windows Controls], ConvertObject method [Windows Controls],IRichEditOle interface, IRichEditOle interface [Windows Controls],ConvertObject method, IRichEditOle.ConvertObject, IRichEditOle::ConvertObject, _win32_IRichEditOle_ConvertObject, _win32_IRichEditOle_ConvertObject_cpp, controls.IRichEditOle_ConvertObject, controls._win32_IRichEditOle_ConvertObject, richole/IRichEditOle::ConvertObject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: richole.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TEXTRANGEW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	IRichEditOle.ConvertObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRichEditOle::ConvertObject


## -description


Converts an object to a new type. This call reloads the object but does not force an update; the caller must do this.


## -parameters




### -param iob

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

Index of the object to convert. If this parameter is REO_IOB_SELECTION, the selected object is to be converted. 


### -param rclsidNew

Type: <b>REFCLSID</b>

Class identifier of the class to which the object is converted. 


### -param lpstrUserTypeNew

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCSTR</a></b>

User-visible type name of the class to which the object is converted. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK on success, or a failure code otherwise. E_INVALIDARG is returned if the index is invalid.




## -see-also




<a href="https://msdn.microsoft.com/d6d1794b-f16c-4a8c-84f5-dfe8bd8be08c">IRichEditOle</a>
 

 

