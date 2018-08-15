---
UID: NF:msi.MsiBeginTransactionW
title: MsiBeginTransactionW function
author: windows-sdk-content
description: The MsiBeginTransaction function starts transaction processing of a multiple-package installation and returns an identifier for the transaction.
old-location: setup\msibegintransaction.htm
old-project: msi
ms.assetid: 05904e58-b24d-4d2c-8b59-a66ad71b494a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MsiBeginTransaction, MsiBeginTransaction function [Setup API], MsiBeginTransactionA, MsiBeginTransactionW, msi/MsiBeginTransaction, msi/MsiBeginTransactionA, msi/MsiBeginTransactionW, setup.msibegintransaction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiBeginTransactionW (Unicode) and MsiBeginTransactionA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DRM_LICENSE_ACQ_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiBeginTransaction
 - MsiBeginTransactionA
 - MsiBeginTransactionW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiBeginTransactionW function


## -description


The  <b>MsiBeginTransaction</b> function starts <a href="t_gly.htm">transaction processing</a> of a multiple-package installation and returns an identifier for the transaction. The  <a href="https://msdn.microsoft.com/70912430-63d7-4087-858c-fb13f47008e2">MsiEndTransaction</a> function ends  the transaction.

<b><a href="https://msdn.microsoft.com/7256b759-3fb5-4195-b0e4-a1631327ebb7">Windows Installer 4.0 and earlier</a>:  </b>Not supported. This function is available beginning with Windows Installer 4.5.


## -parameters




### -param szName [in]

Name of the multiple-package installation.


### -param dwTransactionAttributes [in]

Attributes of the multiple-package installation. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
When 0 or no value is set it Windows Installer closes the UI from the previous installation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>MSITRANSACTION_CHAIN_EMBEDDEDUI</dt>
</dl>
</td>
<td width="60%">
Set this attribute to request that the Windows Installer not shutdown the embedded UI until the transaction is complete.

</td>
</tr>
</table>
 


### -param phTransactionHandle [out]

Transaction ID is a <b>MSIHANDLE</b> value that identifies the transaction. Only one process can own a transaction at a  time.


### -param phChangeOfOwnerEvent [out]

This parameter returns a handle to an event that  is set when the <a href="https://msdn.microsoft.com/222c37fd-1a77-4017-8e55-cbd844f375df">MsiJoinTransaction</a> function changes the owner of the transaction to a new owner. The current owner can use this to determine when ownership of the transaction has changed. Leaving a transaction without an owner will roll back the transaction.


## -returns



The <b>MsiBeginTransaction</b> function returns the following values.
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_SERVICE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The installation service could not be accessed. This function requires the Windows Installer service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSTALL_ALREADY_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
Only one transaction can be open on a system at a time. The function returns this error if  called while another transaction is running.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ROLLBACK_DISABLED</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/6c70e788-beb0-46db-94b0-1bbaac972acf">Rollback Installations</a> have been disabled by the <a href="https://msdn.microsoft.com/c17d9663-af13-4e12-b496-64942f4379f5">DISABLEROLLBACK</a> property or <a href="https://msdn.microsoft.com/01747de6-7478-4403-ba36-8ff1abc2b70f">DisableRollback</a> policy.     

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c4a0f4d8-818d-4e60-908b-adaa2a54de95">Multiple Package Installations</a>
 

 

