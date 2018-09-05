---
UID: NS:winbio_adapter._WINBIO_ENGINE_INTERFACE
title: "_WINBIO_ENGINE_INTERFACE"
author: windows-sdk-content
description: Contains pointers to your custom engine adapter functions.
old-location: secbiomet\winbio_engine_interface.htm
old-project: SecBioMet
ms.assetid: 04429f64-ae41-4c26-a777-bdb7aa92b685
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PWINBIO_ENGINE_INTERFACE, PWINBIO_ENGINE_INTERFACE, PWINBIO_ENGINE_INTERFACE structure pointer [Windows Biometric Framework API], WINBIO_ENGINE_INTERFACE, WINBIO_ENGINE_INTERFACE structure [Windows Biometric Framework API], _WINBIO_ENGINE_INTERFACE, secbiomet.winbio_engine_interface, winbio_adapter/PWINBIO_ENGINE_INTERFACE, winbio_adapter/WINBIO_ENGINE_INTERFACE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winbio_adapter.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: "*PWINBIO_ENGINE_INTERFACE, WINBIO_ENGINE_INTERFACE"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winbio_adapter.h
api_name:
 - WINBIO_ENGINE_INTERFACE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WINBIO_ENGINE_INTERFACE structure


## -description


The <b>WINBIO_ENGINE_INTERFACE</b> structure contains pointers to your custom engine adapter functions. The Windows Biometric Framework uses this structure to locate the functions.


## -struct-fields




### -field Version

Version number of this structure.

<b>Windows 10:  </b>The version number must be <b>WINBIO_ENGINE_INTERFACE_VERSION_3</b> or <b>WINBIO_ENGINE_INTERFACE_VERSION_4</b>. For more information on implementing <b>WINBIO_ENGINE_INTERFACE_VERSION_4</b>, see <a href="https://msdn.microsoft.com/en-us/library/windows/desktop/mt771893(v=vs.85).aspx">Sensor requirements for secure biometrics</a>.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012 and Windows 8:  </b>The version number must be <b>WINBIO_ENGINE_INTERFACE_VERSION_2</b>.

<b>Windows Server 2008 R2 and Windows 7:  </b>The version number must be <b>WINBIO_ENGINE_INTERFACE_VERSION_1</b>.


### -field Type

The type of adapter. This must be <b>WINBIO_ADAPTER_TYPE_ENGINE</b>.


### -field Size

The size, in bytes, of this structure. Set this value to the size of the <b>WINBIO_ENGINE_INTERFACE</b> structure.



### -field AdapterId

A GUID that uniquely identifies the engine adapter. You must generate this value.


### -field Attach

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/e797952b-c7dd-41ad-9536-97d7ce1a7a5d">EngineAdapterAttach</a> function.


### -field Detach

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/a4bc8ef1-6005-4661-9bb1-20ea08d9a125">EngineAdapterDetach</a> function.


### -field ClearContext

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/c4ed5971-e657-4583-aac2-6263801f7468">EngineAdapterClearContext</a> function.


### -field QueryPreferredFormat

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/df76e7d7-9a71-4c98-b038-8925d8cf0980">EngineAdapterQueryPreferredFormat</a> function.


### -field QueryIndexVectorSize

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/07e9f956-1bae-4011-92a0-6c5ed0d105a0">EngineAdapterQueryIndexVectorSize</a> function.


### -field QueryHashAlgorithms

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/66766c80-44b5-4bec-b8cc-32adf1ddae8a">EngineAdapterQueryHashAlgorithms</a> function.


### -field SetHashAlgorithm

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/0d16d82a-287c-4402-ac10-f601684bd976">EngineAdapterSetHashAlgorithm</a> function.


### -field QuerySampleHint

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/9208cd3e-205d-4ef0-8f67-292385dea9a2">EngineAdapterQuerySampleHint</a> function.


### -field AcceptSampleData

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/fa6c5aa4-a9f4-421e-bc43-ced7fade4144">EngineAdapterAcceptSampleData</a> function.


### -field ExportEngineData

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/9ac11720-7dbf-4479-b2c5-78cd53494e21">EngineAdapterExportEngineData</a> function.


### -field VerifyFeatureSet

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/64107d5b-3071-4bd4-9c2c-dd06006aec4d">EngineAdapterVerifyFeatureSet</a> function.


### -field IdentifyFeatureSet

A pointer to your implementation of the   <a href="https://msdn.microsoft.com/838f839d-0bb0-4194-b0a2-ad6936d7b0e4">EngineAdapterIdentifyFeatureSet</a> function.


### -field CreateEnrollment

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/5eec81ec-490c-485f-bbaf-4d972d7c8fde">EngineAdapterCreateEnrollment</a> function.


### -field UpdateEnrollment

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/cd41be8c-fa78-4746-a9ad-c8385ed84b52">EngineAdapterUpdateEnrollment</a> function.


### -field GetEnrollmentStatus

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/cd029d7e-e103-4bbb-aaf9-36f3043b941c">EngineAdapterGetEnrollmentStatus</a> function.


### -field GetEnrollmentHash

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/3a6984a1-0391-4e26-ad92-c07dc066acdb">EngineAdapterGetEnrollmentHash</a> function.


### -field CheckForDuplicate

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/0c73e8b3-2bec-419c-bcb0-3e35d1520f05">EngineAdapterCheckForDuplicate</a> function.


### -field CommitEnrollment

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/f8eb3dd9-b993-4b45-b7f4-e1925c233a80">EngineAdapterCommitEnrollment</a> function.


### -field DiscardEnrollment

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/305540bc-e0c6-460a-a00b-c295b3d6db93">EngineAdapterDiscardEnrollment</a> function.


### -field ControlUnit

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/e0b61709-948f-4adf-8391-b904cf8a1648">EngineAdapterControlUnit</a> function.


### -field ControlUnitPrivileged

A pointer to your implementation of the  <a href="https://msdn.microsoft.com/1d1fda45-3822-40c0-ac84-0fcdef1a6498">EngineAdapterControlUnitPrivileged</a> function.


### -field NotifyPowerChange

A pointer to your implementation of the <a href="https://msdn.microsoft.com/805152AE-CCFE-4C05-8142-F9EF8D124625">EngineAdapterNotifyPowerChange</a> function. This member is supported starting in Windows 8.


### -field Reserved_1

This field is reserved and should be set to <b>NULL</b>.


### -field PipelineInit

A pointer to your implementation of the <a href="https://msdn.microsoft.com/69D4BB35-2E00-4FF6-8A69-DFCEFA5785A0">EngineAdapterPipelineInit</a> function. This member is supported starting in Windows 10.


### -field PipelineCleanup

A pointer to your implementation of the <a href="https://msdn.microsoft.com/C77EBE33-E781-4FFA-BE3A-A08BD9C3D459">EngineAdapterPipelineCleanup</a> function. This member is supported starting in Windows 10.


### -field Activate

A pointer to your implementation of the <a href="https://msdn.microsoft.com/0E98D887-A974-4B86-934E-939DEB1946DF">EngineAdapterActivate</a> function. This member is supported starting in Windows 10.


### -field Deactivate

A pointer to your implementation of the <a href="https://msdn.microsoft.com/A7FDB75C-146C-47E9-AB3B-8457EA3304BF">EngineAdapterDeactivate</a> function.  This member is supported starting in Windows 10.


### -field QueryExtendedInfo

A pointer to your implementation of the <a href="https://msdn.microsoft.com/795547BF-FADE-4AFE-B5DF-1A295F759037">EngineAdapterQueryExtendedInfo</a> function. This member is supported starting in Windows 10.


### -field IdentifyAll

A pointer to your implementation of the <a href="https://msdn.microsoft.com/B8B72654-D161-480B-AD3D-8ED236249562">EngineAdapterIdentifyAll</a> function. This member is supported starting in Windows 10.


### -field SetEnrollmentSelector

A pointer to your implementation of the <a href="https://msdn.microsoft.com/4374F4BA-2B09-4C89-9B5E-CF6B53220A4F">EngineAdapterSetEnrollmentSelector</a> function. This member is supported starting in Windows 10.


### -field SetEnrollmentParameters

A pointer to your implementation of the <a href="https://msdn.microsoft.com/BB353505-F861-47BD-A617-42F0AA39251E">EngineAdapterSetEnrollmentParameters</a> function. This member is supported starting in Windows 10.


### -field QueryExtendedEnrollmentStatus

A pointer to your implementation of the <a href="https://msdn.microsoft.com/E471FC60-9FFC-4269-92A0-7CCA53D3475B">EngineAdapterQueryExtendedEnrollmentStatus</a> function. This member is supported starting in Windows 10.


### -field RefreshCache

A pointer to your implementation of the <a href="https://msdn.microsoft.com/AD0A3BBC-3948-402A-AC3A-96BAF00A164C">EngineAdapterRefreshCache</a> function. This member is supported starting in Windows 10.


### -field SelectCalibrationFormat

A pointer to your implementation of the <a href="https://msdn.microsoft.com/1B4920D9-3C8E-4206-A71B-619A14ADD10A">EngineAdapterSelectCalibrationFormat</a> function. This member is supported starting in Windows 10.


### -field QueryCalibrationData

A pointer to your implementation of the <a href="https://msdn.microsoft.com/2BC0C6D4-931C-4CB8-9620-5F224F8F436F">EngineAdapterQueryCalibrationData</a> function. This member is supported starting in Windows 10.


### -field SetAccountPolicy

A pointer to your implementation of the <a href="https://msdn.microsoft.com/9D2C6CF9-A069-40AD-9BB7-81797F7B2FE6">EngineAdapterSetAccountPolicy</a> function. This member is supported starting in Windows 10.


### -field CreateKey

A pointer to your implementation of the <a href="https://msdn.microsoft.com/3EB42081-6949-46F8-B235-377234A90C39">EngineAdapterCreateKey</a> function. This member is supported starting in Windows 10, version 1607.


### -field IdentifyFeatureSetSecure

A pointer to your implementation of the <a href="https://msdn.microsoft.com/56BD9A75-2779-4D21-A083-75736DE6880E">EngineAdapterIdentifyFeatureSetSecure</a> function. This member is supported starting in Windows 10, version 1607.


### -field AcceptPrivateSensorTypeInfo

 


### -field CreateEnrollmentAuthenticated

 


### -field IdentifyFeatureSetAuthenticated

 




## -see-also




<a href="https://msdn.microsoft.com/5f04d912-f9bc-41d4-aa9e-b843e4b5a994">Plug-in Functions</a>



<a href="https://msdn.microsoft.com/64fb908c-72c2-4639-a2f6-77ede080512c">Plug-in Structures</a>



<a href="https://msdn.microsoft.com/d98da825-ce27-41ec-8f82-6f44e4854018">WbioQueryEngineInterface</a>
 

 

