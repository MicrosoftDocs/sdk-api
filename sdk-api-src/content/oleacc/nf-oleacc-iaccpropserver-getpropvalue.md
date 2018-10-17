---
UID: NF:oleacc.IAccPropServer.GetPropValue
title: IAccPropServer::GetPropValue
author: windows-sdk-content
description: Retrieves a property value for an accessible element.
old-location: winauto\iaccpropserver_iaccpropserver__getpropvalue.htm
tech.root: WinAuto
ms.assetid: 35cb2935-c41b-4588-9199-23789af23b72
ms.author: windowssdkdev
ms.date: 10/16/2018
ms.keywords: GetPropValue, GetPropValue method [Windows Accessibility], GetPropValue method [Windows Accessibility],IAccPropServer interface, IAccPropServer interface [Windows Accessibility],GetPropValue method, IAccPropServer.GetPropValue, IAccPropServer::GetPropValue, _msaa_IAccPropServer_GetPropValue, msaa.iaccpropserver_iaccpropserver__getpropvalue, oleacc/IAccPropServer::GetPropValue, winauto.iaccpropserver_iaccpropserver__getpropvalue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: oleacc.h
req.include-header: OleAcc.h Include Initguid.h first.
req.target-type: Windows
req.target-min-winverclnt: Windows Vista or Windows XP
req.target-min-winversvr: Windows Server 2003
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
req.dll: Oleacc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Oleacc.dll
api_name:
 - IAccPropServer.GetPropValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
---

# IAccPropServer::GetPropValue


## -description


Retrieves a property value for an accessible element.


## -parameters




### -param pIDString [in]

Type: <b>const  BYTE*</b>

Contains a string that identifies the property  being requested.


### -param dwIDStringLen [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Specifies the length of the identity string specified by the <i>pIDString</i> parameter.


### -param idProp [in]

Type: <b>MSAAPROPID</b>

Specifies a GUID indicating the desired property.


### -param pvarValue [out]

Type: <b>VARIANT*</b>

Specifies the value of the overridden property. This parameter is valid only if <i>pfHasProp</i> is <b>TRUE</b>. The server must set this to VT_EMPTY if <i>pfHasProp</i> is set to <b>FALSE</b>.


### -param pfHasProp [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a>*</b>

Indicates whether the server is supplying a value for the requested property. The server should set this to <b>TRUE</b> if it is returning an overriding property or to <b>FALSE</b> if it is not returning a property (in which case it should also set <i>pvarValue</i> to VT_EMPTY).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Return S_OK, except under exceptional error conditions such as low memory. If the specified property is not overridden, then <i>pfHasProp</i> should be set to <b>FALSE</b> and <i>pvarValue</i> should be set to VT_EMPTY by the server.




## -remarks



If a single callback object is registered for annotating multiple accessible elements, the identity string can be used to determine which element this request refers to.

If the accessible element is <b>HWND</b>-based, <a href="https://msdn.microsoft.com/b14932a1-7585-49e4-80eb-498cf48796ee">IAccPropServices::DecomposeHwndIdentityString</a> can be used to extract the HWND/idObject/idChild from the identity string.

If the callback has a value to return for the specified property, it should return it in <i>pvarValue</i> and set <i>pfHasProp</i> to <b>TRUE</b>. Otherwise it should set <i>pvarValue</i> to VT_EMPTY and set <i>pfHasProp</i> to <b>FALSE</b>. In this latter case, the original <a href="https://msdn.microsoft.com/51e95b01-71e7-435b-85fb-28ee43eb08a7">IAccessible</a> interface pointer will be used to obtain a value for this property.



