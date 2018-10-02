---
UID: NE:comadmin.COMAdminTxIsolationLevelOptions
title: COMAdminTxIsolationLevelOptions
author: windows-sdk-content
description: Indicates the isolation level that is to be used for transactions.
old-location: cos\comadmintxisolationleveloptions.htm
tech.root: cossdk
ms.assetid: 5e407423-b116-48c5-a99c-2551eca379b3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: COMAdminTxIsolationLevelAny, COMAdminTxIsolationLevelOptions, COMAdminTxIsolationLevelOptions enumeration [COM+], COMAdminTxIsolationLevelReadCommitted, COMAdminTxIsolationLevelReadUnCommitted, COMAdminTxIsolationLevelRepeatableRead, COMAdminTxIsolationLevelSerializable, _cos_COMAdminTxIsolationLevelOption, comadmin/COMAdminTxIsolationLevelAny, comadmin/COMAdminTxIsolationLevelOptions, comadmin/COMAdminTxIsolationLevelReadCommitted, comadmin/COMAdminTxIsolationLevelReadUnCommitted, comadmin/COMAdminTxIsolationLevelRepeatableRead, comadmin/COMAdminTxIsolationLevelSerializable, cos.comadmintxisolationleveloptions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: comadmin.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ComAdmin.h
api_name:
 - COMAdminTxIsolationLevelOptions
product: Windows
targetos: Windows
req.typenames: COMAdminTxIsolationLevelOptions
req.redist: 
---

# COMAdminTxIsolationLevelOptions enumeration


## -description


Indicates the isolation level that is to be used for transactions.


## -enum-fields




### -field COMAdminTxIsolationLevelAny

Any isolation level is supported. A downstream component that has this isolation level always uses the same isolation level that its immediate upstream component uses. If the root object in a transaction has its isolation level configured to COMAdminTxIsolationLevelAny, its isolation level becomes COMAdminTxIsolationLevelSerializable.


### -field COMAdminTxIsolationLevelReadUnCommitted

A transaction can read any data, even if it is being modified by another transaction. Any type of new data can be inserted during a transaction. This is the least safe isolation level but allows the highest concurrency.


### -field COMAdminTxIsolationLevelReadCommitted

A transaction cannot read data that is being modified by another transaction that has not committed. Any type of new data can be inserted during a transaction. This is the default isolation level in Microsoft SQL Server.


### -field COMAdminTxIsolationLevelRepeatableRead

Data read by a current transaction cannot be changed by another transaction until the current transaction finishes. Any type of new data can be inserted during a transaction.


### -field COMAdminTxIsolationLevelSerializable

Data read by a current transaction cannot be changed by another transaction until the current transaction finishes. No new data can be inserted that would affect the current transaction. This is the safest isolation level and is the default, but allows the lowest level of concurrency.


## -remarks



This enumeration is used to configure the transaction isolation level for components that use transactions. It is also used to configure the isolation level for using the transaction service without components by being passed as a parameter to <a href="https://msdn.microsoft.com/en-us/library/ms681162(v=VS.85).aspx">IServiceTransactionConfigBase::IsolationLevel</a>. This method is called through <a href="https://msdn.microsoft.com/f546ded4-255e-4565-b588-f36175902778">CServiceConfig</a> for either the work submitted through the activity created by <a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a> or the work that is enclosed between calls to <a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a> and <a href="https://msdn.microsoft.com/en-us/library/ms686062(v=VS.85).aspx">CoLeaveServiceDomain</a>.

If a downstream component is configured with a higher isolation level than an upstream component and attempts to enlist in a transaction, an error results and the transaction aborts.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679553(v=VS.85).aspx">CoCreateActivity</a>



<a href="https://msdn.microsoft.com/en-us/library/ms683559(v=VS.85).aspx">CoEnterServiceDomain</a>



<a href="https://msdn.microsoft.com/en-us/library/ms685131(v=VS.85).aspx">Configuring Transaction Isolation Levels</a>
 

 

