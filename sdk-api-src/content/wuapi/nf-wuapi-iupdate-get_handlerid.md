---
UID: NF:wuapi.IUpdate.get_HandlerID
title: IUpdate::get_HandlerID (wuapi.h)
description: Gets the install handler of the update.
helpviewer_keywords: ["HandlerID property [Windows Update Agent]","HandlerID property [Windows Update Agent]","IUpdate interface","IUpdate interface [Windows Update Agent]","HandlerID property","IUpdate.HandlerID","IUpdate.get_HandlerID","IUpdate::HandlerID","IUpdate::get_HandlerID","get_HandlerID","wua.iupdate_handlerid","wuapi/IUpdate::HandlerID","wuapi/IUpdate::get_HandlerID"]
old-location: wua\iupdate_handlerid.htm
tech.root: wua
ms.assetid: af7d4b22-c4e2-4f3d-bef6-5a0cc4f4d5a5
ms.date: 12/05/2018
ms.keywords: HandlerID property [Windows Update Agent], HandlerID property [Windows Update Agent],IUpdate interface, IUpdate interface [Windows Update Agent],HandlerID property, IUpdate.HandlerID, IUpdate.get_HandlerID, IUpdate::HandlerID, IUpdate::get_HandlerID, get_HandlerID, wua.iupdate_handlerid, wuapi/IUpdate::HandlerID, wuapi/IUpdate::get_HandlerID
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdate::get_HandlerID
 - wuapi/IUpdate::get_HandlerID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdate.HandlerID
 - IUpdate.get_HandlerID
---

# IUpdate::get_HandlerID

## -description

Gets the install handler of the update.

This property is read-only.

## -parameters

### -param retval [out, retval]

Type: <b>BSTR*</b>

A pointer to a variable of type <a href="/previous-versions/windows/desktop/automat/bstr">BSTR</a> that receives the identifier of the install handler. The caller must free this memory with the <a href="/windows/win32/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function when it is no longer required.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The valid values for the <b>HandlerID</b> property include the following:

* The Command Line Installation Handler: <code>http://schemas.microsoft.com/msus/2002/12/UpdateHandlers/CommandLineInstallation</code>
* The Inf Based Installation Handler: <code>http://schemas.microsoft.com/msus/2002/12/UpdateHandlers/InfBasedInstallation</code>
* The <a href="/windows/desktop/Msi/windows-installer-portal">Windows Installer</a> Installation Handler: <code>http://schemas.microsoft.com/msus/2002/12/UpdateHandlers/WindowsInstaller</code>
* The Package Installer for Microsoft Windows Operating Systems and Windows Components (update.exe) Installation Handler: <code>http://schemas.microsoft.com/msus/2002/12/UpdateHandlers/WindowsPatch</code>
* The Component Based Servicing (CBS) Handler: <code>http://schemas.microsoft.com/msus/2002/12/UpdateHandlers/Cbs</code>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdate">IUpdate</a>