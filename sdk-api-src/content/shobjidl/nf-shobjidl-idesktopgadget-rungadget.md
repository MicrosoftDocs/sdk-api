---
UID: NF:shobjidl.IDesktopGadget.RunGadget
title: IDesktopGadget::RunGadget (shobjidl.h)
description: Adds an installed gadget to the desktop.
helpviewer_keywords: ["IDesktopGadget interface [Windows Shell]","RunGadget method","IDesktopGadget.RunGadget","IDesktopGadget::RunGadget","RunGadget","RunGadget method [Windows Shell]","RunGadget method [Windows Shell]","IDesktopGadget interface","_shell_IDesktopGadget_RunGadget","shell.IDesktopGadget_RunGadget","shobjidl/IDesktopGadget::RunGadget"]
old-location: shell\IDesktopGadget_RunGadget.htm
tech.root: shell
ms.assetid: 9243fd88-122f-40be-ab71-66c52fa99168
ms.date: 12/05/2018
ms.keywords: IDesktopGadget interface [Windows Shell],RunGadget method, IDesktopGadget.RunGadget, IDesktopGadget::RunGadget, RunGadget, RunGadget method [Windows Shell], RunGadget method [Windows Shell],IDesktopGadget interface, _shell_IDesktopGadget_RunGadget, shell.IDesktopGadget_RunGadget, shobjidl/IDesktopGadget::RunGadget
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDesktopGadget::RunGadget
 - shobjidl/IDesktopGadget::RunGadget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - IDesktopGadget.RunGadget
---

# IDesktopGadget::RunGadget


## -description

Adds an installed gadget to the desktop.

## -parameters

### -param gadgetPath [in]

Type: <b>LPCWSTR</b>

Pointer to the full (absolute) path of a .gadget folder. A gadget that is not packaged with Windows can only be run from one of the two following locations. Installation of the gadget in any other location will cause this method to fail with an access denied error.

                    

<div class="alert"><b>Note</b>  This path should not contain environment variables; the fully expanded path must be provided. <a href="/windows/desktop/api/rrascfg/nn-rrascfg-ieapproviderconfig">ExpandEnvironmentStrings</a> can be used to expand the path to the form required in this parameter.</div>
<div> </div>


#### (%ProgramFiles%\Windows Sidebar\Shared Gadgets)

This is the recommended path for non-Microsoft gadget installation, available to all users.



#### (%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets)

This location should be used for a single-user installation of the gadget.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SCHED_E_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The gadget is already running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An error occurred involving the path of the gadget folder pointed to by <i>gadgetPath</i>.

</td>
</tr>
</table>

## -remarks

"Running" a gadget here means that the gadget is added to the desktop.

<b>RunGadget</b> can only be called on a gadget that has already been installed to the system. It cannot be called on a gadget that is already running—only one instance of a gadget can be run at any given time through this method.

Because gadget installation has no UI of its own, this method is often run as the last step in the installation process or as part of the first launch of an application that the gadget is associated with. Installation of the gadget to %ProgramFiles%\Windows Sidebar\Shared Gadgets requires administrative privileges. Therefore it is recommended that the installation of the gadget be performed as part of a Microsoft Installer (MSI) installation.

<div class="alert"><b>Important</b>  Applications should not call <b>RunGadget</b> without first asking the user for permission. If the choice is given to the user as a check box, that check box should be unselected by default.</div>
<div> </div>
The gadget is added to the desktop at a position determined by the system. The caller cannot specify location.

Per-user applications should install their gadgets per-user. Per-machine applications should install their gadgets per-machine. This ensures a unified experience to the user.


#### Examples

The following example shows <b>IDesktopGadget::RunGadget</b> in use.


```cpp
HRESULT RunMyGadget(PCWSTR pszGadgetPath)
{
    IDesktopGadget *pDG;

    HRESULT hr = CoCreateInstance(CLSID_DesktopGadget, 
                                  NULL, 
                                  CLSCTX_INPROC_SERVER, 
                                  IID_PPV_ARGS(&pDG));
    if (SUCCEEDED(hr))
    {
        hr = pDG->RunGadget(pszGadgetPath);
        pDG->Release();
    }

    return hr;
}
```