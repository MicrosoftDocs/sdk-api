---
UID: NF:mswmdm.IMDSPStorage.SendOpaqueCommand
title: IMDSPStorage::SendOpaqueCommand (mswmdm.h)
description: The SendOpaqueCommands method sends a command through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.
helpviewer_keywords: ["IMDSPStorage interface [windows Media Device Manager]","SendOpaqueCommand method","IMDSPStorage.SendOpaqueCommand","IMDSPStorage::SendOpaqueCommand","IMDSPStorageSendOpaqueCommand","SendOpaqueCommand","SendOpaqueCommand method [windows Media Device Manager]","SendOpaqueCommand method [windows Media Device Manager]","IMDSPStorage interface","mswmdm/IMDSPStorage::SendOpaqueCommand","wmdm.imdspstorage_sendopaquecommands"]
old-location: wmdm\imdspstorage_sendopaquecommands.htm
tech.root: WMDM
ms.assetid: c8a43a21-6ea4-4402-b0fc-2ce7868c83d7
ms.date: 12/05/2018
ms.keywords: IMDSPStorage interface [windows Media Device Manager],SendOpaqueCommand method, IMDSPStorage.SendOpaqueCommand, IMDSPStorage::SendOpaqueCommand, IMDSPStorageSendOpaqueCommand, SendOpaqueCommand, SendOpaqueCommand method [windows Media Device Manager], SendOpaqueCommand method [windows Media Device Manager],IMDSPStorage interface, mswmdm/IMDSPStorage::SendOpaqueCommand, wmdm.imdspstorage_sendopaquecommands
req.header: mswmdm.h
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
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMDSPStorage::SendOpaqueCommand
 - mswmdm/IMDSPStorage::SendOpaqueCommand
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IMDSPStorage.SendOpaqueCommand
---

# IMDSPStorage::SendOpaqueCommand


## -description

The <b>SendOpaqueCommands</b> method sends a command through Windows Media Device Manager. Without acting on it, Windows Media Device Manager passes the command through to a device.

## -parameters

### -param pCommand [in, out]

Pointer to an <b>OPAQUECOMMAND</b> structure containing the information required to execute the command.

## -returns

The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="/windows/desktop/WMDM/error-codes">Error Codes</a>.

## -remarks

This method is used with device commands that do not affect Windows Media Device Manager, and are passed through unchanged.

This method is optional. For more information, see <a href="/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.

## -see-also

<a href="/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage">IMDSPStorage Interface</a>



<a href="/windows/desktop/WMDM/opaquecommand">OPAQUECOMMAND</a>