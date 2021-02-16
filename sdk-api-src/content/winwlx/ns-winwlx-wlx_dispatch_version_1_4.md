---
UID: NS:winwlx._WLX_DISPATCH_VERSION_1_4
title: WLX_DISPATCH_VERSION_1_4 (winwlx.h)
description: Defines the format of the Winlogon version 1.4 function dispatch table passed to the GINA DLL in the WlxInitialize call.
helpviewer_keywords: ["*PWLX_DISPATCH_VERSION_1_4","PWLX_DISPATCH_VERSION_1_4","PWLX_DISPATCH_VERSION_1_4 structure pointer [Security]","WLX_DISPATCH_VERSION_1_4","WLX_DISPATCH_VERSION_1_4 structure [Security]","_gina_wlx_dispatch_version_1_4","security.wlx_dispatch_version_1_4","winwlx/PWLX_DISPATCH_VERSION_1_4","winwlx/WLX_DISPATCH_VERSION_1_4"]
old-location: security\wlx_dispatch_version_1_4.htm
tech.root: security
ms.assetid: b2d0c936-5430-48ed-b808-92209b909406
ms.date: 12/05/2018
ms.keywords: '*PWLX_DISPATCH_VERSION_1_4, PWLX_DISPATCH_VERSION_1_4, PWLX_DISPATCH_VERSION_1_4 structure pointer [Security], WLX_DISPATCH_VERSION_1_4, WLX_DISPATCH_VERSION_1_4 structure [Security], _gina_wlx_dispatch_version_1_4, security.wlx_dispatch_version_1_4, winwlx/PWLX_DISPATCH_VERSION_1_4, winwlx/WLX_DISPATCH_VERSION_1_4'
req.header: winwlx.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WLX_DISPATCH_VERSION_1_4, *PWLX_DISPATCH_VERSION_1_4
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WLX_DISPATCH_VERSION_1_4
 - winwlx/_WLX_DISPATCH_VERSION_1_4
 - PWLX_DISPATCH_VERSION_1_4
 - winwlx/PWLX_DISPATCH_VERSION_1_4
 - WLX_DISPATCH_VERSION_1_4
 - winwlx/WLX_DISPATCH_VERSION_1_4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winwlx.h
api_name:
 - WLX_DISPATCH_VERSION_1_4
---

# WLX_DISPATCH_VERSION_1_4 structure


## -description

The <b>WLX_DISPATCH_VERSION_1_4</b> structure defines the format of the <a href="/windows/desktop/SecGloss/w-gly">Winlogon</a> version 1.4 function dispatch table passed to the <a href="/windows/desktop/SecGloss/g-gly">GINA</a> DLL in the 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxinitialize">WlxInitialize</a> call.

This dispatch table is used if the GINA DLL specifies version 1.4 in its implementation of 
<a href="/windows/desktop/api/winwlx/nf-winwlx-wlxnegotiate">WlxNegotiate</a>.

## -struct-fields

### -field WlxUseCtrlAltDel

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_use_ctrl_alt_del">WlxUseCtrlAltDel</a> function.

### -field WlxSetContextPointer

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_context_pointer">WlxSetContextPointer</a> function.

### -field WlxSasNotify

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_sas_notify">WlxSasNotify</a> function.

### -field WlxSetTimeout

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_timeout">WlxSetTimeout</a> function.

### -field WlxAssignShellProtection

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_assign_shell_protection">WlxAssignShellProtection</a> function.

### -field WlxMessageBox

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_message_box">WlxMessageBox</a> function.

### -field WlxDialogBox

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box">WlxDialogBox</a> function.

### -field WlxDialogBoxParam

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_param">WlxDialogBoxParam</a> function.

### -field WlxDialogBoxIndirect

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect">WlxDialogBoxIndirect</a> function.

### -field WlxDialogBoxIndirectParam

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param">WlxDialogBoxIndirectParam</a> function.

### -field WlxSwitchDesktopToUser

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_switch_desktop_to_user">WlxSwitchDesktopToUser</a> function.

### -field WlxSwitchDesktopToWinlogon

Pointer to a  <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_switch_desktop_to_winlogon">WlxSwitchDesktopToWinlogon</a> function.

### -field WlxChangePasswordNotify

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify">WlxChangePasswordNotify</a> function.

### -field WlxGetSourceDesktop

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_get_source_desktop">WlxGetSourceDesktop</a> function.

### -field WlxSetReturnDesktop

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_return_desktop">WlxSetReturnDesktop</a> function.

### -field WlxCreateUserDesktop

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_create_user_desktop">WlxCreateUserDesktop</a> function.

### -field WlxChangePasswordNotifyEx

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_change_password_notify_ex">WlxChangePasswordNotifyEx</a> function.

### -field WlxCloseUserDesktop

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_close_user_desktop">WlxCloseUserDesktop</a> function.

### -field WlxSetOption

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_set_option">WlxSetOption</a> function.

### -field WlxGetOption

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_get_option">WlxGetOption</a> function.

### -field WlxWin31Migrate

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_win31_migrate">WlxWin31Migrate</a> function.

### -field WlxQueryClientCredentials

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_client_credentials">WlxQueryClientCredentials</a> function.

### -field WlxQueryInetConnectorCredentials

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ic_credentials">WlxQueryInetConnectorCredentials</a> function.

### -field WlxDisconnect

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_disconnect">WlxDisconnect</a> function.

### -field WlxQueryTerminalServicesData

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data">WlxQueryTerminalServicesData</a> function.

### -field WlxQueryConsoleSwitchCredentials

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_consoleswitch_credentials">WlxQueryConsoleSwitchCredentials</a> function.

### -field WlxQueryTsLogonCredentials

Pointer to a <a href="/windows/desktop/api/winwlx/nc-winwlx-pwlx_query_ts_logon_credentials">WlxQueryTsLogonCredentials</a> function.