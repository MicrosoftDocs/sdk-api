---
UID: NF:setupapi.SetupDiInstallClassExA
title: SetupDiInstallClassExA function (setupapi.h)
description: The SetupDiInstallClassEx function installs a class installer or an interface class. (ANSI)
helpviewer_keywords: ["SetupDiInstallClassExA", "di-rtns_80aa5f67-e57e-4749-8130-5c940376db49.xml"]
old-location: devinst\setupdiinstallclassex.htm
tech.root: devinst
ms.assetid: 72ab3fb4-dc4f-439a-87ed-4f4ad061d03a
ms.date: 12/05/2018
ms.keywords: SetupDiInstallClassEx, SetupDiInstallClassEx function [Device and Driver Installation], SetupDiInstallClassExA, SetupDiInstallClassExW, devinst.setupdiinstallclassex, di-rtns_80aa5f67-e57e-4749-8130-5c940376db49.xml, setupapi/SetupDiInstallClassEx
req.header: setupapi.h
req.include-header: Setupapi.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Microsoft Windows 2000 and later versions of Windows.
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
req.lib: Setupapi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupDiInstallClassExA
 - setupapi/SetupDiInstallClassExA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Setupapi.lib
 - Setupapi.dll
api_name:
 - SetupDiInstallClassEx - SetupDiInstallClassExA
---

# SetupDiInstallClassExA function


## -description

The <b>SetupDiInstallClassEx</b> function installs a class installer or an interface class.

## -parameters

### -param hwndParent [in, optional]

The handle to the parent window for any user interface that is used to install this class. This parameter is optional and can be <b>NULL</b>.

### -param InfFileName [in, optional]

A pointer to a NULL-terminated string that contains the name of an INF file. This parameter is optional and can be <b>NULL</b>. If this function is being used to install a class installer, the INF file contains an <a href="/windows-hardware/drivers/install/inf-classinstall32-section">INF ClassInstall32 section</a> and this parameter must not be <b>NULL</b>.

If this function is being used to install an interface class, the INF file contains an <a href="/windows-hardware/drivers/install/inf-interfaceinstall32-section">INF InterfaceInstall32 section</a>.

### -param Flags [in]

A value of type DWORD that controls the installation process. <i>Flags</i> can be zero or a bitwise OR of the following values:





#### DI_NOVCP

Set this flag if <i>FileQueue</i> is supplied. 

DI_NOVCP instructs the <b>SetupInstallFromInfSection</b> function not to create a queue of its own and to use the caller-supplied queue instead. 

If this flag is set, files are not copied just queued. 

For more information about the <b>SetupInstallFromInfSection</b> function, see the Microsoft Windows SDK documentation.



#### DI_NOBROWSE

Set this flag to disable browsing if a copy operation cannot find a specified file. If the caller supplies a file queue, this flag is ignored.



#### DI_FORCECOPY

Set this flag to always copy files, even if they are already present on the user's computer. If the caller supplies a file queue, this flag is ignored.



#### DI_QUIETINSTALL

Set this flag to suppress the user interface unless absolutely necessary. For example, do not display the progress dialog. If the caller supplies a file queue, this flag is ignored.

### -param FileQueue [in, optional]

If the DI_NOVCP flag is set, this parameter supplies a handle to a file queue where file operations should be queued but not committed.

### -param InterfaceClassGuid [in, optional]

A pointer to a GUID that identifies the interface class to be installed. This parameter is optional and can be <b>NULL</b>. If this parameter is specified, this function is being used to install the interface class represented by the GUID. If this parameter is <b>NULL</b>, this function is being used to install a class installer.

### -param Reserved1

Reserved. Must be zero.

### -param Reserved2

Reserved. Must be zero.

## -returns

<b>SetupDiInstallClassEx</b> returns <b>TRUE</b> if it is successful. Otherwise, it returns <b>FALSE</b> and the logged error can be retrieved with a call to <a href="/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The caller of this function must be a member of the Administrators group.

<b>SetupDiInstallClassEx</b> is typically called by a class installer to install a new <a href="/windows-hardware/drivers/install/overview-of-device-setup-classes">device setup class</a> or a new <a href="/windows-hardware/drivers/install/overview-of-device-interface-classes">device interface class</a>. 

<div class="alert"><b>Note</b>  An interface class can also be installed automatically by calling <a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldeviceinterfaces">SetupDiInstallDeviceInterfaces</a> to install the device interfaces for a device.</div>
<div> </div>




> [!NOTE]
> The setupapi.h header defines SetupDiInstallClassEx as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdicallclassinstaller">SetupDiCallClassInstaller</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdiinstalldeviceinterfaces">SetupDiInstallDeviceInterfaces</a>
